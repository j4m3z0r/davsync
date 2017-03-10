# DavSync
DavSync: like rsync, for WebDAV.

# About:
DavSync is a small, self-contained tool for synchronizing local folders with
remote folders via the WebDAV protocol. It requires only Python 2.7, and is
fully contained in the davsync file in order to make it easy to just copy to a
server and start using it.

DavSync was initially developed to facilitate uploading data to
[OpenDrive](https://www.opendrive.com/) from a Synology NAS, and has really
only been tested in this use-case, however it should work with any other WebDAV
compliant server.

DavSync was inspired by the excellent [rsync](https://rsync.samba.org/)
utility, though makes no claim to be as robust or well-engineered as it is.

# Usage:
```
usage: davsync [-h] [-v] [-l LOGIN] [-p PASSWORD] url srcPath dstPath

positional arguments:
  url                   URL to sync with
  srcPath               path to sync from (use "wd:" for remote)
  dstPath               path to sync to (use "wd:" for remote)

optional arguments:
  -h, --help            show this help message and exit
  -v, --verbose         use verbose output
  -l LOGIN, --login LOGIN
                        login username (typically email address)
  -p PASSWORD, --password PASSWORD
                        password for remote server

Example: ./davsync -l username -p password https://site.com photos wd:photos
```

