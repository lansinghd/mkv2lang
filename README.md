# mkv2lang
This (very) simple bash script uses [MKVToolNix](https://mkvtoolnix.download) to find Matroska (mkv) files where the first audio track has an undefined language code `und` and sets the language to a hardcoded value.

`mkv2lang` can be used as a postprocessing script for [Sickrage](https://github.com/SickRage/SickRage) - specify the path to the script within Sickrage postprocessing settings and Sickrage will run the script automatically on postprocessed files.

Note that the script will begin making changes immediately without confirmation. Take care.

## Installation
1. Install [MKVToolNix](https://mkvtoolnix.download/downloads.html) from the MKVToolNix respositories to ensure a recent version is installed.
2. Edit `mkv2lang` to set your preferred default language - run `mkvmerge --list-languages` to see the available language codes.
3. Optional: copy `mkv2lang` to `/usr/local/bin` or somewhere similar for system-wide usage.
4. `chmod +x mkv2lang`
5. Go!

## Usage
* Run recursively in the current folder: `mkv2lang`
* Run recursively in some folder: `mkv2lang /some/folder`
* Run on a single file: `mkv2lang somefile.mkv`
