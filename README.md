cli_file_util
=============

Simple utils for cleaning, archiving, comparing files

A selection of handy CLI file handling utilities.

- addate <file>, addtime <file> is a comfortable way of adding date or
  date+time to a filename. As the purpose is most often archiving, write
  permission is also withdrawn from the file.

- savewdate <file>, savewtime <file> is very similar except it does not modify
  the original filename (nor the permissions), rather makes a copy for
  archiving.

- cleanfn cleans up the most commonly messy filenames in the current directory.

- compdiff <dir> requires a directory as input, and compares files in that
  directory and the current directory with the same filename. Those that are
  different are moved into a "kul" subdirectory and then opened in vimdiff.

- cpcl <file> and mvcl <file> copy and move, respectively, a file to the
  current directory and also copy their new full path into the clipboard. If
  <file> is already in the current directory then only the full path is copied
  into the clipboard. Very handy when you need to make a notice of a file.

- deloldfiles <no> deletes all files older than <no> days. If no <no> is given
  then default is 60 days. HANDLE WITH CARE!

- linkffile <dir> <file> reads <file> until the first space of each line, and
  recursively links files from <dir> with matching filenames to the current
  dir. Asks questions if ambiguous.

- mkrnddir <no> creates a directory with the date and a random string of length
  <no> in its name. If <no> is not given then it defaults to 5. 0 is also
  accepted for <no>. Use as ". mkrnddir" to also change to the new directory.

- nomatch4 <dir> checks if local files are there in <dir> (recursively). Those
  with no match are listed. Filenames don't matter as cmp is used.

I'm no programmer, so please don't blame me on the quality of the code. :-)
Licensed under GNU GPLv3.
