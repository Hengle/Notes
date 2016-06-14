# HTTP Header���
������Լ�����ʵ��һ�� Web Server�������о���һ�� HTTP Э�飬�������� HTTP Header ����ǳ��࣬������ͨ���ʼǵ���ʽ��¼һ�£��������������磬ԭ�ĵ�[����](http://www.zcmhi.com/archives/71.html)

HTTP��HyperTextTransferProtocol�������ı�����Э�飬Ŀǰ��ҳ����ĵ�ͨ��Э�顣

HTTPЭ�����������/��Ӧģ�ͣ�������������ͻ��˷������󣬷�����������Ӧ��������������Դ������ԣ����� message-header �� message-body �����֡����ȴ��� message-header���� http header ��Ϣ��http header ��Ϣͨ������Ϊ 4 �����֣�general header��request header��response header��entity header���������ַַ��������ԣ��о����޲�̫��ȷ������ά���ٿƶ� http header ���ݵ���֯��ʽ�������Ϊ Request �� Response �����֡�

## Requests ����

|Header|����|ʾ��|
|:---:|:---:|:---:|
|Accept|ָ���ͻ����ܹ����ܵ���������|Accept: text/plain, text/html|
|Accept-Charset|��������Խ��ܵ��ַ����뼯|Accept-Charset: iso-8859-5|
|Accept-Encoding|ָ�����������֧�ֵ�web��������������ѹ����������|Accept-Encoding: compress, gzip|
|Accept-Language|������ɽ��ܵ�����|Accept-Language: en,zh|
|Accept-Ranges|����������ҳʵ���һ�����߶���ӷ�Χ�ֶ�|Accept-Ranges: bytes|
|Authorization|HTTP��Ȩ����Ȩ֤��|Authorization: Basic QWxhZGRpbjpvcGVuIHNlc2FtZQ==|
|Cache-Control|ָ���������Ӧ��ѭ�Ļ������|Cache-Control: no-cache|
|Connection|��ʾ�Ƿ���Ҫ�־����ӡ���HTTP 1.1Ĭ�Ͻ��г־����ӣ�|Connection: close|
|Cookie|HTTP������ʱ����ѱ����ڸ����������µ�����cookieֵһ���͸�web������|Cookie: $Version=1; Skin=new;|
|Content-Length|��������ݳ���|Content-Length: 348|
|Date|�����͵����ں�ʱ��|Date: Tue, 15 Nov 2010 08:12:31 GMT|
|Expect|������ض��ķ�������Ϊ|Expect: 100-continue|
|From|����������û���Email|From: user@email.com|
|Host|ָ������ķ������������Ͷ˿ں�|Host: www.zcmhi.com|
|If-Match|ֻ������������ʵ����ƥ�����Ч|If-Match: "737060cd8c284d8af7ad3082f209582d"|
|If-Modified-Since|�������Ĳ�����ָ��ʱ��֮���޸�������ɹ���δ���޸��򷵻�304����|If-Modified-Since: Sat, 29 Oct 2010 19:43:31 GMT|
|If-None-Match|�������δ�ı䷵��304���룬����Ϊ��������ǰ���͵�Etag�����������Ӧ��Etag�Ƚ��ж��Ƿ�ı�|If-None-Match: "737060cd8c284d8af7ad3082f209582d"|
|If-Range|���ʵ��δ�ı䣬���������Ϳͻ��˶�ʧ�Ĳ��֣�����������ʵ�塣����ҲΪEtag|If-Range: "737060cd8c284d8af7ad3082f209582d"|
|If-Unmodified-Since|ֻ��ʵ����ָ��ʱ��֮��δ���޸Ĳ�����ɹ�|If-Unmodified-Since: Sat, 29 Oct 2010 19:43:31 GMT|
|Max-Forwards|������Ϣͨ����������ش��͵�ʱ��|Max-Forwards: 10|
|Pragma|��������ʵ���ض���ָ��|Pragma: no-cache|
|Proxy-Authorization|���ӵ��������Ȩ֤��|Proxy-Authorization: Basic QWxhZGRpbjpvcGVuIHNlc2FtZQ==|
|Range|ֻ����ʵ���һ���֣�ָ����Χ|Range: bytes=500-999|
|Referer|��ǰ��ҳ�ĵ�ַ����ǰ������ҳ������󣬼���·|Referer: http://www.zcmhi.com/archives/71.html|
|TE|�ͻ���Ը����ܵĴ�����룬��֪ͨ���������ܽ���β��ͷ��Ϣ|TE: trailers,deflate;q=0.5|
|Upgrade|�������ָ��ĳ�ִ���Э���Ա����������ת�������֧�֣�|Upgrade: HTTP/2.0, SHTTP/1.3, IRC/6.9, RTA/x11|
|User-Agent|User-Agent�����ݰ�������������û���Ϣ|User-Agent: Mozilla/5.0 (Linux; X11)|
|Via|֪ͨ�м����ػ�����������ַ��ͨ��Э��|Via: 1.0 fred, 1.1 nowhere.com (Apache/1.1)|
|Warning|������Ϣʵ��ľ�����Ϣ|Warn: 199 Miscellaneous warning|

## Responses ����
|Header|����|ʾ��|
|:---:|:---:|:---:|
|Accept-Ranges|�����������Ƿ�֧��ָ����Χ�����������͵ķֶ�����|Accept-Ranges: bytes|
|Age|��ԭʼ���������������γɵĹ���ʱ�䣨����ƣ��Ǹ���|Age: 12|
|Allow|��ĳ������Դ����Ч��������Ϊ���������򷵻�405|Allow: GET, HEAD|
|Cache-Control|�������еĻ�������Ƿ���Ի��漰��������|Cache-Control: no-cache|
|Content-Encoding|web������֧�ֵķ�������ѹ����������|Content-Encoding: gzip|
|Content-Language|��Ӧ�������|Content-Language: en,zh|
|Content-Length|��Ӧ��ĳ���|Content-Length: 348|
|Content-Location|������Դ������ı��õ���һ��ַ|Content-Location: /index.htm|
|Content-MD5|������Դ��MD5У��ֵ|Content-MD5: Q2hlY2sgSW50ZWdyaXR5IQ==|
|Content-Range|�������������б����ֵ��ֽ�λ��|Content-Range: bytes 21010-47021/47022|
|Content-Type|�������ݵ�MIME����|Content-Type: text/html; charset=utf-8|
|Date|ԭʼ��������Ϣ������ʱ��|Date: Tue, 15 Nov 2010 08:12:31 GMT|
|ETag|���������ʵ���ǩ�ĵ�ǰֵ|ETag: "737060cd8c284d8af7ad3082f209582d"|
|Expires|��Ӧ���ڵ����ں�ʱ��|Expires: Thu, 01 Dec 2010 16:00:00 GMT|
|Last-Modified|������Դ������޸�ʱ��|Last-Modified: Tue, 15 Nov 2010 12:45:26 GMT|
|Location|�����ض�����շ���������URL��λ��<hr>�����������ʶ�µ���Դ|Location: http://www.zcmhi.com/archives/94.html|
|Pragma|����ʵ���ض���ָ�����Ӧ�õ���Ӧ���ϵ��κν��շ�|Pragma: no-cache|
|Proxy-Authenticate|��ָ����֤�����Ϳ�Ӧ�õ�����ĸ�URL�ϵĲ���|Proxy-Authenticate: Basic|
|refresh|Ӧ�����ض����һ���µ���Դ�����죬��5��֮���ض�����������������󲿷������֧�֣�|Refresh: 5; url=http://www.zcmhi.com/archives/94.html|
|Retry-After|���ʵ����ʱ����ȡ��֪ͨ�ͻ�����ָ��ʱ��֮���ٴγ���|Retry-After: 120|
|Server|web�������������|Server: Apache/1.3.27 (Unix) (Red-Hat/Linux)|
|Set-Cookie|����Http Cookie|Set-Cookie: UserID=JohnDoe; Max-Age=3600; Version=1|
|Trailer|ָ��ͷ���ڷֿ鴫������β������|Trailer: Max-Forwards|
|Transfer-Encoding|�ļ��������|Transfer-Encoding:chunked|
|Vary|�������δ�����ʹ�û�����Ӧ���Ǵ�ԭʼ����������|Vary: *|
|Via|��֪����ͻ�����Ӧ��ͨ�����﷢�͵�|Via: 1.0 fred, 1.1 nowhere.com (Apache/1.1)|
|Warning|����ʵ����ܴ��ڵ�����|Warning: 199 Miscellaneous warning|
|WWW-Authenticate|�����ͻ�������ʵ��Ӧ��ʹ�õ���Ȩ����|WWW-Authenticate: Basic|

����μ� w3c ���� [Header Field Definitions](http://www.w3.org/Protocols/rfc2616/rfc2616-sec14.html)