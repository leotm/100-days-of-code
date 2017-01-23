# 100 Days Of Code - Log

**Link(s) to work**

### Day 21: January 23, 2017

**Today's Progress**: 
Solved the freeCodeCamp *Slasher Flick* algorithm challenge.
Solved the freeCodeCamp *Mutations* algorithm challenge.

**Thoughts** 
Slasher Flick:
An *unshift()* loop sprang to mind, but probably not the best:
```
function slasher(arr, howMany) {
  for (var i = 0; i < howMany; i++) {
    arr.shift();
  }
  return arr;
}
```
Otherwise, no need to loop with *splice()*.

Mutation challenge:

Spent way too long on this one. Debugging each test case in DevTools until passed. I initially tried searching each target letter contains the search letter. This got it to pass 8/9 test cases, but not the last. This is when I realised, it's pointless counting the number of hits and misses for each target letter. I need to do it the other way round. Count the number of hits for each search letter. Much better. DevTools snippets - I love you.

**Link(s) to work**
[freecodecamp.com/leotm | Basic Algorithm Scripting | Slasher Flick](https://www.freecodecamp.com/challenges/slasher-flick#?solution=%0Afunction%20slasher(arr%2C%20howMany)%20%7B%0A%20%20arr.splice(0%2C%20howMany)%3B%0A%20%20return%20arr%3B%0A%7D%0A%0A%2F%2F%20Test%20case%0Aslasher(%5B1%2C%202%2C%203%5D%2C%202)%3B)

[freecodecamp.com/leotm | Basic Algorithm Scripting | Mutations](https://www.freecodecamp.com/challenges/mutations#?solution=%0A%20%20function%20mutation(arr)%20%7B%0A%20%20%20%20var%20misses%20%3D%200%3B%0A%20%20%20%20var%20totalMatches%20%3D%200%3B%0A%20%20%20%20for%20(var%20i%20%3D%200%3B%20i%20%3C%20arr%5B1%5D.length%3B%20i%2B%2B)%20%7B%20%2F%2F%20For%20each%20search%20letter%0A%20%20%20%20%20%20for%20(var%20j%20%3D%200%3B%20j%20%3C%20arr%5B0%5D.length%3B%20j%2B%2B)%20%7B%20%2F%2F%20For%20each%20target%20letter%0A%20%20%20%20%20%20%20%20if%20(arr%5B1%5D%5Bi%5D.toLowerCase().indexOf(arr%5B0%5D%5Bj%5D.toLowerCase())%20%3D%3D%3D%20-1)%20%7B%0A%20%20%20%20%20%20%20%20%20%20misses%2B%2B%3B%0A%20%20%20%20%20%20%20%20%20%20if%20(misses%20%3D%3D%3D%20arr%5B0%5D.length)%20%7B%0A%20%20%20%20%20%20%20%20%20%20%20%20return%20false%3B%20%2F%2F%20No%20match%0A%20%20%20%20%20%20%20%20%20%20%7D%0A%20%20%20%20%20%20%20%20%7D%20else%20%7B%0A%20%20%20%20%20%20%20%20%20%20%2F%2F%20Match%0A%20%20%20%20%20%20%20%20%20%20misses%20%3D%200%3B%20%2F%2F%20Reset%20for%20next%20iteration%0A%20%20%20%20%20%20%20%20%20%20break%3B%20%2F%2F%20Since%20no%20need%20to%20search%20the%20rest%0A%20%20%20%20%20%20%20%20%7D%0A%20%20%20%20%20%20%7D%0A%20%20%20%20%7D%0A%20%20%20%20return%20true%3B%0A%20%20%7D%0A%0A%2F%2F%20Test%20case%0Amutation(%5B%22floor%22%2C%20%22for%22%5D)%3B)

### Day 20: January 22, 2017

**Today's Progress**: 
Solved the freeCodeCamp *Chunky Monkey* algorithm challenge.

**Thoughts** 
Failed with this one. Tried nested *for* loop create new array, each time the *index % num === 0*. But you can't *push* to an undefined index. Then accepted the hint it became obvious, slice then push.

**Link(s) to work**
[freecodecamp.com/leotm | Basic Algorithm Scripting | Chunky Monkey](https://www.freecodecamp.com/challenges/chunky-monkey#?solution=%0Afunction%20chunkArrayInGroups(arr%2C%20size)%20%7B%0A%20%20var%20groupsArray%20%3D%20%5B%5D%3B%0A%20%20for%20(var%20i%20%3D%200%3B%20i%20%3C%20arr.length%3B%20i%20%2B%3D%20size)%20%7B%0A%20%20%20%20groupsArray.push(arr.slice(i%2C%20i%2Bsize))%3B%0A%20%20%7D%0A%20%20return%20groupsArray%3B%0A%7D%0A%0AchunkArrayInGroups(%5B%22a%22%2C%20%22b%22%2C%20%22c%22%2C%20%22d%22%5D%2C%202)%3B%0A)

### Day 19: January 21, 2017

**Today's Progress**: 
Solved the freeCodeCamp *Truncate a string* algorithm challenge.

**Thoughts** 
Pretty straight forward again.

**Link(s) to work**
[freecodecamp.com/leotm | Basic Algorithm Scripting | Truncate a string](https://www.freecodecamp.com/challenges/truncate-a-string#?solution=%0Afunction%20truncateString(str%2C%20num)%20%7B%0A%20%20if%20(str.length%20%3E%20num)%20%7B%0A%20%20%20%20if%20(num%20%3C%3D%203)%20%7B%0A%20%20%20%20%20%20return%20str.slice(0%2C%20num)%20%2B%20%22...%22%3B%0A%20%20%20%20%7D%20else%20%7B%0A%20%20%20%20%20%20return%20str.slice(0%2C%20num-3)%20%2B%20%22...%22%3B%0A%20%20%20%20%7D%0A%20%20%7D%20else%20%7B%0A%20%20%20%20return%20str%3B%0A%20%20%7D%0A%7D%0A%0A%2F%2F%20Test%20case%0AtruncateString(%22Hello%22%2C%2010)%3B%0A)

### Day 18: January 20, 2017

**Today's Progress**: 
Solved the freeCodeCamp *Repeat a string repeat a string* algorithm challenge.

**Thoughts** 
Pretty straight forward again.

**Link(s) to work**
[freecodecamp.com/leotm | Basic Algorithm Scripting | Repeat a string repeat a string](https://www.freecodecamp.com/challenges/repeat-a-string-repeat-a-string#?solution=%0Afunction%20repeatStringNumTimes(str%2C%20num)%20%7B%0A%20%20var%20arr%20%3D%20%5B%5D%3B%0A%20%20for%20(var%20i%20%3D%200%3B%20i%20%3C%20num%3B%20i%2B%2B)%20%7B%0A%20%20%20%20arr.push(str)%3B%0A%20%20%7D%0A%20%20return%20arr.join(%22%22)%3B%0A%7D%0A%0A%2F%2F%20Test%20case%0ArepeatStringNumTimes(%22abc%22%2C%203)%3B)

### Day 17: January 19, 2017

**Today's Progress**: 
Solved the freeCodeCamp *Confirm the Ending* algorithm challenge.

**Thoughts** 
Pretty straight forward.

**Link(s) to work**
[freecodecamp.com/leotm | Basic Algorithm Scripting | Confirm the Ending](https://www.freecodecamp.com/challenges/confirm-the-ending#?solution=%0Afunction%20confirmEnding(str%2C%20target)%20%7B%0A%20%20return%20(str.substring(str.length-target.length%2C%20str.length)%20%3D%3D%3D%20target)%3B%0A%7D%0A%0AconfirmEnding(%22Bastian%22%2C%20%22n%22)%3B%0A)

### Day 16: January 18, 2017

**Today's Progress**: 
Solved the freeCodeCamp *Return Largest Numbers in Arrays* algorithm challenge.

**Thoughts** 
Nearly had it. Didn't pass the 2nd test case.
Copied the code into a Chrome Dev Tools snippet, proceeded to debug.
Realised I forgot to clear/reset *largest* variable per loop, otherwise it will remember the largest number from the previous array.
Debugging wins.

**Link(s) to work**
[freecodecamp.com/leotm | Basic Algorithm Scripting | Return Largest Numbers in Arrays](https://www.freecodecamp.com/challenges/return-largest-numbers-in-arrays#?solution=%0Afunction%20largestOfFour(arr)%20%7B%0A%20%20var%20largest%20%3D%200%3B%0A%20%20for%20(var%20i%20%3D%200%3B%20i%20%3C%20arr.length%3B%20i%2B%2B)%20%7B%20%2F%2F%20For%20each%20array%0A%20%20%20%20for%20(var%20j%20%3D%200%3B%20j%20%3C%20arr%5Bi%5D.length%3B%20j%2B%2B)%20%7B%20%2F%2F%20For%20each%20number%0A%20%20%20%20%20%20if%20(arr%5Bi%5D%5Bj%5D%20%3E%20largest)%20%7B%0A%20%20%20%20%20%20%20%20largest%20%3D%20arr%5Bi%5D%5Bj%5D%3B%20%2F%2F%20Store%20largest%20number%0A%20%20%20%20%20%20%7D%0A%20%20%20%20%7D%0A%20%20%20%20arr%5Bi%5D%20%3D%20largest%3B%20%2F%2F%20Assign%20largest%20number%0A%20%20%20%20largest%20%3D%200%3B%20%2F%2F%20Clear%20largest%20number%0A%20%20%7D%0A%20%20return%20arr%3B%0A%7D%0A%0A%2F%2F%20Test%20case%0AlargestOfFour(%5B%5B13%2C%2027%2C%2018%2C%2026%5D%2C%20%5B4%2C%205%2C%201%2C%203%5D%2C%20%5B32%2C%2035%2C%2037%2C%2039%5D%2C%20%5B1000%2C%201001%2C%20857%2C%201%5D%5D)%3B)

### Day 15: January 17, 2017

**Today's Progress**: 
Solved the freeCodeCamp *Title Case a Sentence* algorithm challenge.

**Thoughts** 
I totally failed today. For a couple hours. Taking a break, works pretty damn well.
Initially misunderstood the challenge, quickly giving an ideal to solution to return the only the first letters of each word, capitalised.
What cost me like an hour? Using array.push(" "), adding a last character, increasing the array size, creating an infinite loop, since the nested *for* loop is looping through each character of each word.
Unforts I repeated code in my solution, since I can't whack *break*s inside functions (invalid). Damn.
May revisit later.

**Link(s) to work**
[freecodecamp.com/leotm | Basic Algorithm Scripting | Title Case a Sentence](https://www.freecodecamp.com/challenges/title-case-a-sentence#?solution=%0Afunction%20titleCase(str)%20%7B%0A%20%20%2F%2F%20Split%20into%20words%0A%20%20str%20%3D%20str.split(%22%20%22)%3B%0A%20%20arr%20%3D%20%5B%5D%3B%0A%20%20%2F%2F%20For%20each%20word%0A%20%20for%20(var%20i%20%3D%200%3B%20i%20%3C%20str.length%3B%20i%2B%2B)%20%7B%0A%20%20%20%20str%5Bi%5D%20%3D%20str%5Bi%5D.split(%22%22)%3B%0A%20%20%20%20%2F%2F%20For%20each%20letter%0A%20%20%20%20for%20(var%20j%20%3D%200%3B%20j%20%3C%20str%5Bi%5D.length%3B%20j%2B%2B)%20%7B%0A%20%20%20%20%20%20%2F%2F%20If%20first%20letter%0A%20%20%20%20%20%20if%20(j%20%3D%3D%3D%200)%20%7B%0A%20%20%20%20%20%20%20%20%2F%2F%20Capitalise%20it%0A%20%20%20%20%20%20%20%20str%5Bi%5D%5Bj%5D%20%3D%20str%5Bi%5D%5Bj%5D.toUpperCase()%3B%0A%20%20%20%20%20%20%20%20%2F%2F%20If%20last%20letter%20of%20word%0A%20%20%20%20%20%20%20%20if%20(j%20%3D%3D%3D%20str%5Bi%5D.length-1)%20%7B%0A%20%20%20%20%20%20%20%20%20%20%2F%2F%20And%20not%20last%20word%0A%20%20%20%20%20%20%20%20%20%20if%20(i%20!%3D%3D%20str.length-1)%20%7B%0A%20%20%20%20%20%20%20%20%20%20%20%20%2F%2F%20Add%20a%20space%0A%20%20%20%20%20%20%20%20%20%20%20%20str%5Bi%5D.push(%22%20%22)%3B%0A%20%20%20%20%20%20%20%20%20%20%20%20break%3B%0A%20%20%20%20%20%20%20%20%20%20%7D%0A%20%20%20%20%20%20%20%20%7D%0A%20%20%20%20%20%20%20%20%2F%2F%20If%20other%20remaining%20letter%0A%20%20%20%20%20%20%7D%20else%20%7B%0A%20%20%20%20%20%20%20%20%2F%2F%20Make%20lower%20case%0A%20%20%20%20%20%20%20%20str%5Bi%5D%5Bj%5D%20%3D%20str%5Bi%5D%5Bj%5D.toLowerCase()%3B%0A%20%20%20%20%20%20%20%20%2F%2F%20If%20last%20letter%20of%20word%0A%20%20%20%20%20%20%20%20if%20(j%20%3D%3D%3D%20str%5Bi%5D.length-1)%20%7B%0A%20%20%20%20%20%20%20%20%20%20%2F%2F%20And%20not%20last%20word%0A%20%20%20%20%20%20%20%20%20%20if%20(i%20!%3D%3D%20str.length-1)%20%7B%0A%20%20%20%20%20%20%20%20%20%20%20%20%2F%2F%20Add%20a%20space%0A%20%20%20%20%20%20%20%20%20%20%20%20str%5Bi%5D.push(%22%20%22)%3B%0A%20%20%20%20%20%20%20%20%20%20%20%20break%3B%0A%20%20%20%20%20%20%20%20%20%20%7D%0A%20%20%20%20%20%20%20%20%7D%0A%20%20%20%20%20%20%7D%0A%20%20%20%20%7D%20%2F%2F%20end%20of%20for%20j%0A%20%20%20%20str%5Bi%5D%20%3D%20str%5Bi%5D.join(%22%22)%3B%0A%20%20%20%20arr.push(str%5Bi%5D)%3B%0A%20%20%7D%20%2F%2F%20end%20of%20for%20i%0A%20%20return%20arr.join(%22%22)%3B%0A%7D%20%2F%2F%20end%20of%20fun%0A%0AtitleCase(%22a%22)%3B)

### Day 14: January 16, 2017

**Today's Progress**: 
Solved the freeCodeCamp *Find the Longest Word in a String* algorithm challenge.

**Thoughts** 
Fairly straight forward.

**Link(s) to work**
[freecodecamp.com/leotm | Basic Algorithm Scripting | Find the Longest Word in a String](https://www.freecodecamp.com/challenges/find-the-longest-word-in-a-string#?solution=function%20findLongestWord(str)%20%7B%0A%20%20%2F%2F%20Split%20string%0A%20%20str%20%3D%20str.split(%22%20%22)%3B%0A%20%20%2F%2F%20Declare%20longest%20word%0A%20%20var%20longestWord%20%3D%200%3B%0A%20%20%2F%2F%20For%20each%20word%0A%20%20for%20(var%20i%20%3D%200%3B%20i%20%3C%20str.length%3B%20i%2B%2B)%20%7B%0A%20%20%20%20%2F%2F%20If%20current%20word%20is%20longer%20than%20stored%20longest%20word%0A%20%20%20%20if%20(str%5Bi%5D.length%20%3E%20longestWord)%20%7B%0A%20%20%20%20%20%20%2F%2F%20Store%20it%0A%20%20%20%20%20%20longestWord%20%3D%20str%5Bi%5D.length%3B%0A%20%20%20%20%7D%0A%20%20%7D%0A%20%20return%20longestWord%3B%0A%7D%0A%0A%2F%2F%20Test%20case%0AfindLongestWord(%22The%20quick%20brown%20fox%20jumped%20over%20the%20lazy%20dog%22)%3B)

### Day 13: January 15, 2017

**Today's Progress**: 
Solved the freeCodeCamp *Check for Palindromes* algorithm challenge.

**Thoughts** 
So it seems, when:
var a = ["l","e","o"];
var b = a;
a.reverse() // or b.reverse()
// Both are reversed. So may need to copy with a.splice()
// But if either array is changed, the link is broken, .reverse() will no longer reverse both

**Link(s) to work**
[freecodecamp.com/leotm | Basic Algorithm Scripting | Check for Palindromes](https://www.freecodecamp.com/challenges/check-for-palindromes#?solution=function%20palindrome(str)%20%7B%0A%20%20%2F%2F%20Remove%20non-alphanumeric%20characters%0A%20%20%2F%2F%20%5CW%20leaves%20the%20underscore%0A%20%20%2F%2F%20A%20short%20equivalent%20for%20%5B%5Ea-zA-Z0-9%5D%20would%20be%20%5B%5CW_%5D%0A%20%20%2F%2F%20%5CW%20is%20the%20negation%20of%20shorthand%20%5Cw%20for%20%5BA-Za-z0-9_%5D%20word%20characters%20(including%20the%20underscore)%0A%20%20str%20%3D%20str.replace(%2F%5B%5CW_%5D%2B%2Fg%2C%22%22)%3B%0A%20%20%2F%2F%20Convert%20to%20lower%20case%0A%20%20str%20%3D%20str.toLowerCase()%3B%0A%20%20%2F%2F%20Copy%20and%20store%20original%2C%20for%20comparison%20later%0A%20%20var%20orig%20%3D%20str.slice()%3B%0A%20%20%2F%2F%20Split%20to%20array%0A%20%20str%20%3D%20str.split(%22%22)%3B%0A%20%20%2F%2F%20Reverse%0A%20%20str.reverse()%3B%0A%20%20%2F%2F%20Join%0A%20%20str%20%3D%20str.join(%22%22)%3B%0A%20%20%2F%2F%20Return%20if%20equals%20original%0A%20%20return%20orig%20%3D%3D%3D%20str%3B%0A%7D%0A%0Apalindrome(%22_eye%22)%3B)

### Day 12: January 14, 2017

**Today's Progress**: 
Solved the freeCodeCamp *Factorialize a Number* algorithm challenge.

**Thoughts** 
Failed on *Factorialize a Number*, using *for* loop to *push* an array of numbers 1 to N, then using *reduce*, prev * cur. Forgot about recursion.

**Link(s) to work**
[freecodecamp.com/leotm | Basic Algorithm Scripting | Factorialize a Number](https://www.freecodecamp.com/challenges/factorialize-a-number#?solution=function%20factorialize(num)%20%7B%0A%20%20%2F%2F%20To%20handle%20the%20case%20where%20num%20%3D%200%0A%20%20if%20(num%20%3D%3D%3D%200)%20%7B%0A%20%20%20%20return%201%3B%0A%20%20%7D%0A%20%20%2F%2F%20Return%20recursive%20answer%20until%20num%20%3D%200%0A%20%20return%20num%20*%20factorialize(num-1)%3B%0A%7D%0A%2F%2F%20Test%20case%0Afactorialize(5)%3B)

### Day 11: January 13, 2017

**Today's Progress**: 
Finished 23 freeCodeCamp excercises.
Finished *Basic JavaScript*.
Started *Basic Algorithm Scripting*.

**Thoughts** 
Was good to come across JS *match()*, since only used regex in Sublime to find/replace.
Wasn't aware *contructor function* was the term.
Nice recapping *Array* functions.
*Reverse a String* was fairly straight forward.

**Link(s) to work**
[freecodecamp.com/leotm](https://www.freecodecamp.com/leotm)

### Day 10: January 12, 2017

**Today's Progress**: 
Finished 26 freeCodeCamp excercises.

**Thoughts** 
Learnt the term *lookup table*, to consider instead of *switch*'s and *if/else*'s statements.
*Profile Lookup* had me a while, plus the early hours of the morning. Silly me, nesting a return statement inside a for loop of a function, so it might not reach the final iteration. Replaced it with a counter instead, then after the loop, return if the counter's reached.

**Link(s) to work**
[freecodecamp.com/leotm](https://www.freecodecamp.com/leotm)

### Day 9: January 11, 2017

**Today's Progress**: 
Finished 25 freeCodeCamp excercises.

**Thoughts** 
Haven't really used the JS *delete* keyword much.
So I'm reminded Math.random() gives those long-ass decimal. So *toFixed()* not compulsory for decimal format.
*Generate Random Whole Numbers within a Range* had me a while again, because ofc I'd rather derive formula myself. Checking Math.round() as a minimum like *0.01* reminded me of the *+1* part.

**Link(s) to work**
[freecodecamp.com/leotm](https://www.freecodecamp.com/leotm)

### Day 8: January 10, 2017

**Today's Progress**: 
Started *Basic JavaScript*.
Finished 25 freeCodeCamp excercises.

**Thoughts** 
So JS String values are *immutable*. Daaayum.

**Link(s) to work**
[freecodecamp.com/leotm](https://www.freecodecamp.com/leotm)

### Day 7: January 9, 2017

**Today's Progress**: 
Finished 40 freeCodeCamp excercises.
Finished *jQuery*.
Finished *Basic Front End Development Projects*.

**Thoughts** 
Learnt some things, and good refresher.
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
I opened a FreeCodeCamp account a while ago, because Quincy Larson gives practical advice. But I didn't go much further, thinking it seems like another Codecademy. After hearing everyone talk on #Open2017, I thought fine - if it turns out to be easy, let's blast through them. A little refresher can't hurt, can maybe learn a thing or two along the way, and the certificates could be nice bonus. Today was mostly simple HTML5 & CSS.
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
