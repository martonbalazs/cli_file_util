cli_file_util
=============

Simple utils for cleaning, archiving, comparing files

A selection of handy CLI file handling utilities.

- addate [file] is a comfortable way of adding date, date+time, or comments to
  a filename. Default is the last modification date of the file but with a
  press of a button the current date or date+time can also be set. Comment might
  also be inserted in the filename as well. As the purpose is most often
  archiving, write permission is also withdrawn from the file.

- savewdate [file] is very similar except it does not modify the original
  filename (nor the permissions), rather makes a copy for archiving.

- cleanfn cleans up the most commonly messy filenames in the current directory.

- compdiff [dir] requires a directory as input, and compares files in that
  directory and the current directory with the same filename. Those that are
  different are moved into a "kul" subdirectory and then opened in vimdiff.

- cpcl [file] and mvcl [file] copy and move, respectively, a file to the
  current directory and also copy their new full path into the clipboard. If
  [file] is already in the current directory then only the full path is copied
  into the clipboard. Very handy when you need to make a notice of a file. If no
  file is given then only pwd is put into xclipboard. Versions lcpcl anv lmvcl do
  the same without clipboarding the path.

- cpfn [file or dir] and mvfn [file or dir] copies or moves a file or a dir
  allowing to comfortably edit its name. It requires vipe.
  
- deloldfiles [no] deletes all files older than [no] days. If no [no] is given
  then default is 60 days. HANDLE WITH CARE!

- linkffile [dir] [file] reads [file] until the first space of each line, and
  recursively links files to the current dir if it read full paths or else from
  [dir] with matching filenames. Asks questions if ambiguous.

- mkrnddir [no] creates a directory with the date and a random string of length
  [no] in its name. If [no] is not given then it defaults to 5. 0 is also
  accepted for [no]. Use as ". mkrnddir" to also change to the new directory.

- nomatch4 [dir] checks if local files are there in [dir] recursively. Those
  with a match are separated in a directory. Filenames don't matter as cmp is used.

I'm no programmer, so please don't blame me on the quality of the code. :-)
Licensed under GNU GPLv3.
