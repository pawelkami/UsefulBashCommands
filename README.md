# UsefulBashCommands

-------------

Repository contains useful bash commands.



#### Hexdump of a file

> xxd -f file | tr -d '\n'



#### Encode all files in current directory with UTF-8

> vim "+set nomore" "+bufdo set fileencoding=utf8 | w" "+q" $(find . -type f)



#### Find and replace string in all files in directory

> find . -print -exec sed -i.bak 's/original/new/g' {} \;
