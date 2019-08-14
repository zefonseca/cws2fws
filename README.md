# cws2fws

CWS to FWS Flash file Decompressor

cws2fws is a short Perl script I wrote to convert CWS compressed Flash v. >= 6 files to FWS files. 

The motivation behind this script was to be able to use the SWF::Search module which currently does not open compressed CWS files.

### How does it work?

cws2fws FILENAME.swf reads the first 8 bytes of FILENAME.swf substituting the CWS header for FWS. 

It then reads from byte 9 to EOF decompressing the stream via the zlib uncompress interface. 

The resulting decompressed stream and the new FWS header are then concatenated to output a file called FILENAME.fws.swf

### License

c2s2fws is licensed under the MIT license. 

See the COPYING file which must be included in this distribution. 

### Author

Jose Fonseca (https://zefonseca.com/)