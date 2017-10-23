# Python-Crawler-Tutorial-URLError
爬虫URLError异常处理  
我们知道，HTTPError的父类是URLError，根据编程经验，父类的异常应当写到子类异常的后面，如果子类捕获不到，那么可以捕获父类的异常</br>
`import urllib2`

`req = urllib2.Request('http://blog.csdn.net/cqcre')`</br>
`try:`</br>
 `   urllib2.urlopen(req)`</br>
`except urllib2.HTTPError, e:`</br>
`    print e.code`</br>
`except urllib2.URLError, e:`</br>
`    print e.reason`</br></br>
`else:`</br>
`    print "OK"`</br>

如果捕获到了HTTPError，则输出code，不会再处理URLError异常。如果发生的不是HTTPError，则会去捕获URLError异常，输出错误原因。

### HTTPError，对应相应的状态吗，HTTP状态码表示HTTP协议所返回的响应的状态。下面将状态码归结如下：
<http://cuiqingcai.com/961.html>
