# VIM

#基础篇
    :e filename Open filename for edition
    :w  Save file
    :q  Exit Vim
    :q! Quit without saving
    :x  Write file (if changes has been made) and exit
    :sav filename   Saves file as filename
    .   Repeats the last change made in normal mode
    5.  Repeats 5 times the last change made in normal mode

    提醒你一下，
        :e filename 可以打开多个文件，切换方法为 ctrl+shift+^
    再提醒你一下，
        :e .   可以看看当前目录有哪些东西
在文件中移动

k or Up Arrow   move the cursor up one line
j or Down Arrow move the cursor down one line
e   move the cursor to the end of the word
b   move the cursor to the begining of the word
0   move the cursor to the begining of the line
G   move the cursor to the end of the line
gg  move the cursor to the begining of the file
L   move the cursor to the end of the file
:59 move cursor to line 59. Replace 59 by the desired line number.
20| move cursor to column 20.
%   Move cursor to matching parenthesis
[[  Jump to function start
[{  Jump to block start

    提醒你一下，
    ctrl+b,ctrl+e,ctrl+f 都可以试一试哦

#剪切、复制和粘贴
y   Copy the selected text to clipboard
p   Paste clipboard contents
dd  Cut current line
yy  Copy current line
y$  Copy to end of line
D   Cut to end of line

    提醒你一下，
        还可以 3yy,复制 3 行
    再提醒一下，使用标记可以复制一个范围的，比如挪到某行 ma  另外一行 mb
        然后:'a,'by  可复制 a 到 b 直接的内容

#搜索
/word   Search word from top to bottom
?word   Search word from bottom to top
Search the word under cursor
/\cstring   Search STRING or string, case insensitive
/jo[ha]n    Search john or joan
/< the  Search the, theatre or then
/the>   Search the or breathe
/< the> Search the
/< ¦.>  Search all words of 4 letters
//  Search fred but not alfred or frederick
/fred|joe   Search fred or joe
/<\d\d\d\d> Search exactly 4 digits
/^\n{3} Find 3 empty lines
:bufdo /searchstr/  Search in all open files
bufdo %s/something/somethingelse/g  Search something in all the open buffers and replace it with somethingelse

    没看明白？
    /\<the\> 只选 the 这个单词

#替换
:%s/old/new/g   Replace all occurences of old by new in file
:%s/onward/forward/gi   Replace onward by forward, case unsensitive
:%s/old/new/gc  Replace all occurences with confirmation
:2,35s/old/new/g    Replace all occurences between lines 2 and 35
:5,$s/old/new/g Replace all occurences from line 5 to EOF
:%s/^/hello/g   Replace the begining of each line by hello
:%s/$/Harry/g   Replace the end of each line by HarryI
:%s/onward/forward/gi   Replace onward by forward, case unsensitive
:%s/ *$//g  Delete all white spaces
:g/string/d Delete all lines containing string
:v/string/d Delete all lines containing which didn ’ t contain string
:s/Bill/Steve/  Replace the first occurence of Bill by Steve in current line
:s/Bill/Steve/g Replace Bill by Steve in current line
:%s/Bill/Steve/g    Replace Bill by Steve in all the file
:%s/^M//g   Delete DOS carriage returns (^M)
:%s/\r/\r/g Transform DOS carriage returns in returns

    可能有的人找这种删除命令很久了
    :g/string/d

