
# How to build Deluge and dependencies 100% from source:

- You need to have installed:

  - Visual Studio 2017
  - [Python](https://www.python.org/ftp/python/3.7.5/python-3.7.5-amd64.exe)
  - [nasm](https://www.nasm.us/pub/nasm/releasebuilds/2.14.02/win64/nasm-2.14.02-installer-x64.exe)
  - [ActivePerl](https://platform.activestate.com/ActiveState/ActivePerl-5.28/auto-fork?utm_campaign=fork-perl&utm_medium=website&utm_source=activestate.com&utm_term=perl5.28&utm_content=fork-activeperl5.28)

- Download the following .zip files : 

  - [boost](https://dl.bintray.com/boostorg/release/1.70.0/source/boost_1_70_0.zip)
  - [openssl](https://github.com/openssl/openssl/archive/master.zip)
  - [gvsbuild](https://github.com/cas--/gvsbuild/archive/master.zip)
  - [Libtorrent](https://github.com/arvidn/libtorrent/archive/RC_1_2.zip)
  - [Deluge](https://github.com/deluge-torrent/deluge/archive/develop.zip)

  and extract each of these archives to a seperate folder in `C:\`   
  and the gvsbuild [master.zip](https://github.com/cas--/gvsbuild/archive/master.zip) to `C:\gtk-build\github` .
  
- Make sure the following are in your `PATH` environment variable:

  ```text
  C:\Perl64\site\bin
  C:\Perl64\bin
  C:\Python\Python37
  C:\Python\Python37\Scripts
  C:\gtk-build\gtk\x64\release\bin
  ```

- Now run the following batch files in the given order:

  ```text
  OpenSSLBuild.bat

  LibtorrentBuild.bat
  
  GTK3Build.bat
  
  DelugeBuild.bat
  ```

- Finally you may run `deluge.exe` via cmd/powershell, or create a shortcut from `C:\Python\Python37\Scripts` .
