# Project 8 - Pentesting Live Targets

Time spent: 7 hours spent in total

> Objective: Identify vulnerabilities in three different versions of the Globitek website: blue, green, and red.

The six possible exploits are:
* Username Enumeration
* Insecure Direct Object Reference (IDOR)
* SQL Injection (SQLi)
* Cross-Site Scripting (XSS)
* Cross-Site Request Forgery (CSRF)
* Session Hijacking/Fixation

Each version of the site has been given two of the six vulnerabilities. (In other words, all six of the exploits should be assignable to one of the sites.)

## Blue

Vulnerability #1: SQL Injection

Gif:

Discussion:

Without loging in, you can go to the 'Find a Salesperson' tab. You then click on any salesperson and can view the id: Id=XX. You can add ' OR SLEEP(5)=0--' to the end of the URL. This SQL Injection causes the site to load for 5 seconds, as shown by the little tab shown at the bottom of the screen. 

Vulnerability #2: Session Hijacking/Fixation:

Gif:

Discussion: 

In this, you open the red version of the site in one web brower and the session change PHP. You then login as admin and get the session add. In another browser, you go to the blue version of the site. You change it's session id and the change the url of the blue site, so that you're not at the login page but at the index page. This site lets you into the page, even though you didn't login. 

## Green

Vulnerability #1: Username Enumeration

Gif:

Discussion: 

Hever you can see that a registered user, if he/she fails to login correctly, the error is shown in bold, whereas for an unregistered user, it's not shwon in bold. 

Vulnerability #2: Cross-Site Scripting (XSS)
Gif:

Discussion:

Here a person can go to the contact tab and type <script>alert('Meghna found the XSS!');</script> into the feedback. When a user logs in and goes to see the feedback, they'll see the XSS alert.


## Red

Vulnerability #1: Insecure Direct Object Reference (IDOR)

Gif:

Discussion:
When we login as admin, we can see the two salesperson, whose information should not be made visible. We can get their id number (id 10 and 11).

As a unregistered user, I could go to the list of salesperson and chlick on one. I could then change their id and replace it to 10 or 11, and see the salesperson's information. 


Vulnerability #2: Cross-Site Request Forgery (CSRF)

Gif:

Discussion:


## Notes

Describe any challenges encountered while doing the work
