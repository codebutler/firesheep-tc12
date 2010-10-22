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
* Cookies literally shouted through the air.
* Someone just has to start listening.

!SLIDE command incremental
# sudo tcpdump -A -i en1 tcp port 80

!SLIDE code
# Request #
(Minecraft HTTP Login, cleaned up)

POST /game/getversion.jsp HTTP/1.1
Content-Type: application/x-www-form-urlencoded
Content-Length: 40
Content-Language: en-US
Cache-Control: no-cache
Pragma: no-cache
User-Agent: Java/1.6.0_20
Host: www.minecraft.net
Accept: text/html, image/gif, image/jpeg, *; q=.2, */*; q=.2
Connection: keep-alive


user=craSH&password=o_hai_t00rc0n!&version=12



!SLIDE code
# Response #
(Minecraft HTTP Login, cleaned up)

HTTP/1.1 200 OK
Server: Resin/3.1.9
Cache-Control: private
Set-Cookie: JSESSIONID=abcdW_m35A6oTgWH2L6Ts; path=/
Content-Type: text/html
Transfer-Encoding: chunked
Date: Tue, 05 Oct 2010 04:12:44 GMT

0010
User not premium
0


!SLIDE bullets incremental
# "Session hijacking"
* "sidejacking?"

