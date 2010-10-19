!SLIDE bullets incremental
# Stealing cookies is easy.

!SLIDE command incremental
# $ sudo tcpdump -i en1 tcp port 80

!SLIDE bullets incremental
# Ferret and Hamster
* Blackhat
* Lots of media: wapo, zdnet, etc... (LIST OUT HERE)
* That was in 2007!

!SLIDE bullets incremental
# Almost nothing has improved
* Gmail good
* Hotmail, Yahoo, still bad.

!SLIDE bullets incremental
# Stealing cookies is easy.
* But not easy enough?

!SLIDE bullets incremental
# Firesheep

!SLIDE 
# Firefox extension

!SLIDE 
# *One-click* session hijacking

!SLIDE
# Step 1
(screenshot of capture button)

!SLIDE 
# Step 2
(screenshot 2)

!SLIDE bullets incremental
# There is no step 3.
* Profit?

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
    
!SLIDE bullets
* Free
* Open Source 
* Mac OS X
* Linux

!SLIDE bullets incremental
# Easy
* Even a tech journalist should be able to do it.
* (But let us know if you need help)

!SLIDE bullets
# Available Now
* Download @ http://URLHERE