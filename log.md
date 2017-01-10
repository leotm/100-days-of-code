# 100 Days Of Code - Log

### Day 7: January 9, 2017

**Today's Progress**: 
Finished 40 FreeCodeCamp excercises.

**Thoughts** 
Finished jQuery, learnt some things, and good refresher.
Whipped up a quick tribute page. Haven't the *jumbotron*, *caption* nor *offset* before.
Since I already have a portfolio, spent 15 minutes inspecting the source code of the example.
Got through 1/4 of Basic JS.

**Link(s) to work**
[freecodecamp.com/leotm](https://www.freecodecamp.com/leotm)

### Day 6: January 8, 2017

**Today's Progress**: 
Configured SSH with my bro to remotely control our boiler via his Python scripts and my Raspberry Pi & spare parts.

**Thoughts** 
Again, something a little today.
Skyped for a couple hours. Chose a port to open, and forwarded that on the router (not 22 :D).
Had to debug why my Terminal when hanging when trying to SSH on my Mac. Turned out to be when the correct port was forwarded, but the Pi hadn't saved the new open port when rebooting.
Learnt *tmux*, to open a session, run the .py script, then leave the session open with *ctrl+b* then *d*, to keep the script running as a background process.
To to kill the scripts, I'm thinking we could: open the session, kill the process; kill the session; kill the process directly with *pkill*. Will stick to the session way for now.
Learnt *top* to view processes. I've used *ps -ef* and *ps aux*, pipelined with *grep* to find them.
Currently have scripts to test the boiler for few secs, turn it on/off, and on 1/2 hrs.
Felt good controlling the boiler remotely.

**Link(s) to work**
[Here's the Tweet with a Photo](https://twitter.com/Leo_T_M/status/818239703845576704)

### Day 5: January 7, 2017

**Today's Progress**:
Finished 27 FreeCodeCamp excercises.
Introduced myself on the forum, read others'.
Joined the LinkedIn Alumni network.

**Thoughts**
Finished Responsive Design with Bootstrap, easy stuff.
Found interesting tales on the forum, will keep checking it out.
Happy to donate to nonprofits again, once I find the right role, the search continues.

**Link(s) to work**
[freecodecamp.com/leotm](https://www.freecodecamp.com/leotm)

### Day 4: January 6, 2017

**Today's Progress**: 
Signed up to HackerRank. Solved 4 Challenges.

**Thoughts** 
Something a little different today.
Came across HackerRank, so let's try that.
Started their 30 Days of Code. Nearly put off by it being in C, until realised could change the language to JS.
Nearly put off again thinking it won't work with these stdin's, but pain is part of the game, got it working, started solving.
Failed some test cases, bought some with Hackos, fixed my code to pass them all.
Since have to wait for the remaining challenges to unlock, did a Database challenge.

**Link(s) to work**
[hackerrank.com/leotm](https://www.hackerrank.com/LeoTM)

### Day 3: January 5, 2017

**Today's Progress**:
Finished 39 FreeCodeCamp excercises.
Watched last half of #Open2017

**Thoughts**
Finished the HTML5 & CSS section, then 1/4 of the Responsive Design with Bootstrap.
Bit of a grind, mostly just skipping to the tasks, dopamine hits galore.

**Link(s) to work**
[freecodecamp.com/leotm](https://www.freecodecamp.com/leotm)

### Day 2: January 4, 2017

**Today's Progress**:
Finished 27 FreeCodeCamp exercises.
Enrolled on [The Nature of Code](https://www.kadenze.com/courses/the-nature-of-code/info)
Watched the first half of #Open2017

**Thoughts**
I opened a FreeCodeCamp account a while ago, because Quincy Larson gives practical advice. But I didn't go much further, thinking it seems like another Codecademy. After hearing everyone talk on #Open2017, I thought fine - if it turns out to be easy, let's blast through them. A little refresher can't hurt, I'm sure I can learn a thing or two along the way, and the certificates could be nice bonus. Today was mostly simple HTML5 & CSS.
I came across [The 10 best free online courses of 2016 according to the data
](https://medium.freecodecamp.com/best-free-online-courses-of-2016-c479b55ed851#.olacxjwzg), checked out [The Nature of Code](https://www.class-central.com/mooc/3777/kadenze-the-nature-of-code), and just had to enroll.

**Link(s) to work**
[freecodecamp.com/leotm](https://www.freecodecamp.com/leotm)

### Day 1: January 3, 2017

**Today's Progress**:
Migrated my Ghost Blog from AWS to Digital Ocean, then setup Let's Encrypt

**Thoughts:**
So I noticed my AWS trial ran out and I've been billed a couple times. As part of the Entrepaneur First program, we got Digital Ocean free credit, so time I decided to migrate to that.
My plan was to just SSH into AWS and backup my Ghost folder, easy peezy. Nope. I made the mistake of deleting my original AWS .pem file, thinking I could just create a new one and authenticate with that - since I'm so comfortable with keypairs and that.
Well, I can no longer SSH, locked out of my AWS.
[replacing lost key pair](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-key-pairs.html#replacing-lost-key-pair) unfortunately involves creating a new instance which will cost more.
So how do I backup my blog posts? Fortuantely after logging in I found the option to back up all posts as .json. Boom, AWS instance now terminated.
Digital Ocean One-click apps made it a breeze to create a Ghost 0.11.3 Droplet on Ubuntu 16.04 x64. Of course, I'm authenticating with a private keypair.
Now, my site [netsca.pe](http://netsca.pe) is hosted with Namecheap. I by mistake bought a year's hosting with them instead of renewing my domain. They refused to process a refund, even within 5 minutes of contacting them immediately. So I refuse to purchase their SSL certificate. But I want HTTPS. This Let's Encrypt thing sounds good. Oh wait, they limit their SSH access so I can't do it. Meh. I'll create a subdomain instead, point it to Digital Ocean, and setup Let's Encrypt there.
So I find the [the right tutorial](https://www.digitalocean.com/community/tutorials/how-to-secure-apache-with-let-s-encrypt-on-ubuntu-16-04), for nginx (I've only used Apache before), and Ubuntu 16.04. Of course the mysql_secure_installation part isn't straight forward, to I finally figure it out and store what I did in a [gist](https://gist.github.com/leotm/0c6c0df98dc5854854e880e7e03b2055) to write up an updated tutorial later. Woop.

**Link(s) to work**
[blog.netsca.pe](https://blog.netsca.pe)
