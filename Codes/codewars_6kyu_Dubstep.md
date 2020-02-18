Dubstep - Javascript
====================

### Input
#### The input consists of a single non-empty string, consisting only of uppercase English letters, the string's length doesn't exceed 200 characters
### Output
#### Return the words of the initial song that Polycarpus used to make a dubsteb remix. Separate the words with a space.
### Example
<pre><code>
songDecoder("WUBWEWUBAREWUBWUBTHEWUBCHAMPIONSWUBMYWUBFRIENDWUB")
// =>  WE ARE THE CHAMPIONS MY FRIEND
</code></pre>

### my code
<pre>
<code>
 function songDecoder(song){
   
   /* 첫번째 답
   while(song.indexOf("WUB") > -1)	{
   	song = song.replace("WUB", " ");
   }
 
   while(song.indexOf("  ") > -1)	{
   	song = song.replace("  ", " ");
   }
   
   if(song.indexOf(" ") == 0  )	{
   	song = song.replace(" ", "");	
   }
 
   if(song.charAt(song.length-1) == " ")	{
   	song = song.slice(0, -1);
   }
   return song;
   */
 
   // 최종답 
   song = song.split("WUB").join(" ");
   song = song.split("  ").join(" ");
 
   if(song.indexOf(" ") == 0  )	{
   	song = song.replace(" ", "");	
   }
 
   if(song.charAt(song.length-1) == " ")	{
   	song = song.slice(0, -1);
   }
   return song;
 }
</code>
</pre>
#### 부끄럽다.... 
#### 가장 멋져 보이는 답
<pre><code>
 function songDecoder(song){
   return song.replace(/(WUB)+/g," ").trim()
 }
 </code></pre>
#### 이 또한 멋진답
<pre><code>
 function songDecoder(song){
   return song.split('WUB').filter(Boolean).join(' ');
 }
</code></pre>

