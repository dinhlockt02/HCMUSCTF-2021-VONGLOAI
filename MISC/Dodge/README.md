Ban đầu ta test thử thì thấy ta có thể sử dụng lệnh ls và lệnh echo
Ta có thể sử dụng lệnh shell thay cho cat
  while read line; do
    echo $line;
  done <flag.txt
flag: 
Tham khảo: https://jarv.org/posts/cat-without-cat/
