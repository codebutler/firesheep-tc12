!SLIDE bullets incremental
# Widely known problem

!SLIDE center
![Elephant in the room](elephant_rave.jpg)

!SLIDE bullets incremental
# Enough is enough.
* How to make people understand risk?

!SLIDE bullets incremental
# Firesheep

!SLIDE
# Firefox extension

!SLIDE bullets incremental
# *One-click* session hijacking

!SLIDE center bullets
* (TODO: Screenshot in stopped state)

!SLIDE center bullets
* (TODO: Screenshot in started state)

!SLIDE center bullets
* (TODO: Screenshot of hijacked session)

!SLIDE
# Extensible via javascript

!SLIDE code
    @@@ javascript
    register({
      name: 'Hacker News',
      domains: [ 'news.ycombinator.com' ],
      sessionCookieNames: [ 'user' ],

      identifyUser: function () {
        var resp = this.httpGet(this.siteUrl);
        this.userName = resp.body
          .querySelectorAll(".pagetop a")[7]
          .textContent;
      }
    });
    
!SLIDE bullets incremental
# Firesheep
* Free
* Open Source 
* Mac OS X
* Windows (Beta)
* Linux (Soon)

!SLIDE bullets
# Available Now
* Download @ http://URLHERE
