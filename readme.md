# Glacier Split File script

I made this back around July 2017 because i was using glacier a lot at the time
to back up a 60GB photo library.  The other utils i found out there didn't
fit the needs i had (cli, stable, does everything).  

Amazon has a util in Java (or C#) that will get the treehas of the file but
for splitting the file and automating the upload etc. they don't really offer
anything, or didn't at the time.

This bash script will:
- get the treehash
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
