!SLIDE bullets incremental
# Stealing cookies is easy.

!SLIDE command incremental
# $ sudo tcpdump -A -i en1 tcp port 80

!SLIDE bullets incremental
# Ferret and Hamster
* Blackhat
* Pretty easy for us hackers to use
* Lots of media: wapo, zdnet, etc... (TODO: LIST OUT HERE)
* That was in 2007!

!SLIDE bullets incremental
# Almost nothing has improved
* Gmail good. Wordpress making smart decisions.
* Hotmail, Yahoo, countless others - still bad.

!SLIDE bullets incremental
# Stealing cookies is easy.
* But not easy enough?

!SLIDE bullets incremental
# Firesheep

!SLIDE
# Firefox extension

!SLIDE bullets incremental
# *One-click* session hijacking
* HTTP Session-hijacking for the masses.

!SLIDE center
# Step 1
TODO: Screenshot in stopped state

!SLIDE center
# Step 2
TODO: Screenshot in started state

!SLIDE bullets incremental
# Step 3.
* There is no step 3.
* Profit?

!SLIDE center
TODO: Screenshot of prefs

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
