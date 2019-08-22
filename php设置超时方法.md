写php程序时，php调用外部接口时会设置超时，现在讲一下如何设置超时

### fsockopen
#### 连接超时
fsockopen()和stream_socket_client() 都可以设置
#### 获取响应数据超时（连接已经成功）  
stream_set_timeout()来设置

### curl
#### 连接超时
curl_setopt 中选项CURLOPT_CONNECTTIMEOUT  
#### 总超时
curl_setopt 中选项CURLOPT_TIMEOUT  
curl 没有设置响应超时的选项，这个总超时的设置时间包含了连接超时的时间  
参考链接：[curl timeout的区别](https://stackoverflow.com/questions/27776129/php-curl-curlopt-connecttimeout-vs-curlopt-timeout)

