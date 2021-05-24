# Dodge
Ban đầu ta test thử thì thấy ta có thể sử dụng lệnh ls và lệnh echo.<br/>
Ta có thể sử dụng lệnh shell thay cho cat
```shell
  while read line; do
    echo $line;
  done <flag.txt
```
flag: HCMUS-CTF{You_know_some_command_line_stuff}<br/>
Tham khảo: https://jarv.org/posts/cat-without-cat/
