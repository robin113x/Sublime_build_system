# Sublime Build System Tool

## Java
{ 
"target": "terminus_exec",
"cancel": "terminus_cancel_build",
"shell_cmd": "javac $file && java $file_base_name<inp.in>out.in",
"working_dir": "$file_path"
}

## Python

{
  "cmd" : ["python3 $file_name -o $file_base_name 4s ./$file_base_name<inp.in>out.in"], 
  "selector" : "source.py",
  "shell": true,
  "working_dir" : "$file_path"
}

## C++
{
  "cmd" : ["g++-10 $file_name -o $file_base_name &&  ./$file_base_name<inp.in>out.in"], 
  "selector" : "source.c,source.cpp",
  "shell": true,
  "working_dir" : "$file_path"
}

//
## RUST
{ 
"target": "terminus_exec",
"shell_cmd": "rustc $file  -o $file_base_name &&  ./$file_base_name<inp.in>out.in",
"working_dir": "$file_path"
}


## C
{
  "cmd" : ["gcc  $file_name -o $file_base_name &&  ./$file_base_name<inp.in>out.in"], 
  "selector" : "source.c,source.cpp",
  "shell": true,
  "working_dir" : "$file_path"
}


## Windows CPP
{
"cmd": ["g++.exe","-std=c++14", "${file}", "-o", "${file_base_name}", "&&" , "${file_base_name}<inp.in>out.in"],
"selector":"source.cpp",
"file_regex": "^(..[^:]*):([0-9]+):?([0-9]+)?:? (.*)$",
"shell":true,
"working_dir":"$file_path"
}



---> for unlimited user license in linux
file bash "sublime_text" is in /opt/sublime_text/sublime_text
first go to site https://hexed.it/
click on Open file and put file "sublime_text"
go to section Search in left of page
put 80 78 05 00 0F 94 C1 in label Search for
then click on Find next
after find it then change if one by one to C6 40 05 01 48 85 C9
after that click on Export
then write this command in terminal
