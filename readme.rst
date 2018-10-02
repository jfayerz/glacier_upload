=========================
Glacier Split File script
=========================

I made this back around July 2017 because I was using Glacier a lot at the time
to back up a 60GB photo library.  The other utils I found out there didn't
fit the needs I had (cli, stable, does everything).  

Amazon has a util in Java (or C#) that will get the treehash of the file. However,
for splitting the file and automating the upload etc. they don't really offer
anything, or didn't at the time.

This bash script will:
- get the treehash (using ruby)
- make various directories and log files for storing information
- split the file (you can specify how large the pieces will be) in the script
- initiate the upload
- upload the files
- finalize/close the aws job for the upload
- record the information given back to it by aws

It does work, with smaller files.  I tried it on my 60GB file once on an old
Mac Mini with 4GB of RAM, and it appeared to freeze things up.  This is
probably not the best way to go about doing this.  Feel free to fork things and
make use of it however you would like.

Note: source code has lots of comments etc. Sorry for being so verbose in
there.

Note2: I made this with what I knew at the time: Bash.  It was for a very specific need that I had.  In the future I may pick this back up and redevelop it using something more along the lines of Rust or Python.
