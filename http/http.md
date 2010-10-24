!SLIDE bullets incremental
# HTTP #

* Request, Response
* Send username/password once
* Receive cookie
* Use cookie for all future requests

!SLIDE
# "Logged In"

!SLIDE bullets incremental
# Cookies need to be kept secret
* But they usually aren't.

!SLIDE bullets incremental
# WiFi
* Cookies shouted through the air.
* Someone just has to start listening.

!SLIDE command incremental
# $ sudo tcpdump -A -i en1 tcp port 80

!SLIDE code
# Request #
    POST /login.php?login_attempt=1 HTTP/1.1
    Host: login.facebook.com

<pre>email=<b>sheep@example.com</b>&amp;pass=<b>supersecure</b></pre>
    
!SLIDE code
# Response #
<pre>HTTP/1.1 302 Found
Location: http://www.facebook.com/home.php?
Set-Cookie: xs=<b>b1cac66e11145bc79847a98f98a6a19c</b>; path=/; domain=.facebook.com; httponly
</pre>

!SLIDE bullets incremental
# "Session hijacking"
* "sidejacking"

