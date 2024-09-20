# php_fcgi_mem
## 0x01 简介
基于<font style="color:rgb(51, 51, 51);">PHP-FPM的内存马，可利用127.0.0.1:9000和unix:///run/php/php7.4-fpm.sock形式的连接。</font>

## 0x02 使用步骤
1、上传该webshell

2、用post方式传参host和port

注：i、当host为<font style="color:rgb(51, 51, 51);">unix:///run/php/php7.4-fpm.sock这种形式时，需要port=-1</font>

<font style="color:rgb(51, 51, 51);">ii、需要从phpinfo里查看auto_append_file的值是否被修改（由于PHP-FPM存在多个进程，上述步骤最好多次发包，保证每个进程都被注入内存马）</font>

3、最后直接使用蚁剑连接，密码test（或者自行修改文件里的base64的内容）

## 0x03 参考
[https://xz.aliyun.com/t/11651](https://xz.aliyun.com/t/11651)

[https://github.com/BeichenDream/Godzilla](https://github.com/BeichenDream/Godzilla)

