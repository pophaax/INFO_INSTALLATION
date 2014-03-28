INFO_INSTALLATION
=================

If you want to install all the libraries onto a new Raspberry Pi
a.k.a. newly formatted Raspberry Pi please follow guidelines below
on which libraries you will need. 
Guidelines are of course towards running a Linux environment on the Raspberry Pi.

This document was last updated 18 Feb 2014.

================================================================
GPS
================================================

  libgps-dev (library)
  
    sudo apt-get install libgps-dev
    
  gpsd (driver)
  
    sudo apt-get install gpsd
================================================
MySQL
================================================
  mysqlclient
  
    git clone https://github.com/pophaax/mysql_client_lib
    
Get all the libraries from github, this will get you a folder called usr Inside usr you have the folders: bin, include, lib, share - which contains the files you need to copy/add into the R Pi's usr folder.

================================================
SQLite - note, links may change at any time
================================================
  get lastest link at http://www.sqlite.org/download.html, then download with
  
    wget http://sqlite.org/2013/sqlite-autoconf-3071602.tar.gz
    
  extract
  
    tar xvf sqlite-autoconf-3071602.tar.gz

  config in extracted folder, first copy/paste:
  
      ./configure --prefix=/usr --disable-static    \
      CFLAGS="-O2" &&
      
  press enter and write:
  
    make
  
  install by:
  
    sudo make install

================================================
Getting all repositories from github
================================================

If you visit https://github.com/pophaax?tab=repositories you'll get a good overview of all the repositories needed for the program.

================================================
