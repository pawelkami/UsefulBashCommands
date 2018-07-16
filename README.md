# UsefulBashCommands



-------------



Repository contains useful bash commands.







#### Hexdump of a file



> xxd -f file | tr -d '\n'







#### Encode all files in current directory with UTF-8



> vim "+set nomore" "+bufdo set fileencoding=utf8 | w" "+q" $(find . -type f)



or

> find . -type f -exec ./recodeifneeded new_encoding {} \\;



*recodeifneeded* is bash script which is also in this repository.

*new_encoding* - for example *utf-8*



#### Find and replace string in all files in directory



> find . -print -exec sed -i.bak 's/original/new/g' {} \\;

or

> grep -rl oldtext . | xargs sed -i 's/oldtext/newtext/g'

