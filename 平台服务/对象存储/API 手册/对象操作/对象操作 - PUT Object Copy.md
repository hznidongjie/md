# 对象操作
## 拷贝对象 - PUT Object Copy

### 描述
远程拷贝操作，生成一个新的对象，相当于”一次GET”+”一次PUT”。

### 语法

    PUT /${DestinationObjectKey} HTTP/1.1
    HOST: ${DestinationBucketName}.${endpoint}
    Date: ${date}
    x-nos-copy-source: /${SourceBucketName}/${SourceObjectKey}
    Authorization: ${signature}

### 请求头

|       Header      |                                                 描述                                                | 是否必须 |
|-------------------|-----------------------------------------------------------------------------------------------------|----------|
| x-nos-copy-source | 拷贝的源对象<br>类型：字符串<br>默认：无<br>限制：该字符串必须做一下 URL Encode，并且对该桶有读权限 | Yes      |

### 示例
Request

    PUT /2.jpg HTTP/1.1
    HOST: photo.nos-eastchina1.126.net
    Date: Fri, 10 Feb 2012 21:34:55 GMT
    x-nos-move-source: /dream/1.jpg
    Authorization: NOS I_AM_ACCESS_ID:I_AM_SIGNATURE

Response

    HTTP/1.1 200 OK
    x-nos-request-id: 17b21e42ac11000001390ab891440240
    Date: Wed, 01 Mar 2012 21:34:55 GMT
    Connection: close
    Server: NOS