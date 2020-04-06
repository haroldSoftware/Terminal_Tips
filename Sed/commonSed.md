## Common Use Cases of Sed (Stream Editor) Command

# sed OPTIONS... [SCRIPT] [INPUTFILE...]

-----
1) Substitute a string \
$ sed 's/replaced/replacedBy' [INPUTFILE]
-----
2) Substitute the nth occurance of a pattern in a line \
$ sed 's/replaced/replacedBy/2' [INPUTFILE]
-----
3) Substitute all occurances of a pattern in a line \
$ sed 's/replaced/replacedBy/g' [INPUTFILE]
-----
4) Substitute from nth occurance to all occurances in a line
(in this case n = 5, so from 5 onwards) \
$ sed 's/replaced/replacedBy/5g' [INPUTFILE]
-----
5) Substitute string on nth line
(in this case the 5th line) \
$ sed '5 s/replaced/replacedBy/' [INPUTFILE]
-----
6) When substituting, print each line substituted
(p is the 'print' flag) \
$ sed '5 s/replaced/replacedBy/p' [INPUTFILE]
-----
7) When substituting, print only the lines substituted
(the -n option and the /p flag prints replaced lines only once) \
$ sed '5 s/replaced/replacedBy/p' [INPUTFILE]
-----
8) Substitute a string within a range
(in this case from 1 to 5) \
$ sed '1,5 s/replaced/replacedBy/' [INPUTFILE] \
(in the following case from 2 to the end, $ is the end) \
$ sed '2,$ s/replaced/replacedBy/' [INPUTFILE]
-----
9) Delete a line from a INPUTFILE
(in this case, the line is the string "s") \
$ sed 'sd' [INPUTFILE]
-----
10) Delete last line from a INPUTFILE \
$ sed '$d' [INPUTFILE]
-----
11) Delete a range of lines from a INPUTFILE
(in this case from x to y lines) \
$ sed 'x,yd' [INPUTFILE]
-----
12) Delete from nth line to end of INPUTFILE
(in this case nth line is 5) \  
$ sed '5,$d' [INPUTFILE]
-----
13) Delete a matching pattern
(in this case the pattern is abc) \
$ sed '/abc/d' [INPUTFILE]
