# REST API

## 通用响应头

|      Header      |                                                             描述                                                            |
|------------------|-----------------------------------------------------------------------------------------------------------------------------|
| Content-Length   | 响应体的字节数<br>类型：字符串<br>默认：无                                                                                  |
| Connection       | 到服务器的连接是否打开<br>类型：枚举类型<br>可选值：keep-alive/close<br>默认：无                                            |
| Date             | 响应的时间戳<br>类型：字符串<br>默认：无                                                                                    |
| ETag             | HTTP Entity Tag，代表对象的哈希值，反应对象内容的更改情况。([RFC2616](http://www.ietf.org/rfc/rfc2616.txt))<br>类型：字符串 |
| Server           | 响应的服务器名称<br>类型： 字符串                                                                                           |
| x-nos-request-id | 唯一定位一个请求的 ID 号，主要用于某些情况下错误定位<br>类型：字符串                                                           |

