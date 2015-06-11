![Definition of Passion] (images/definition.png)
---

![Web/App Intersection] (images/PassionDiagram.png)

If you think about it, web apps and native apps seem to go about things in completely opposite ways.  The web server runs remotely and serves up pages; the native app runs locally and pulls down data.  One is written in Ruby, HTML, CSS and Javascript while the other is written in Swift or Java. 

Different architectures, different languages, yet it's the same app.  These days we must support both Web and Mobile. What can be done?  My passion project will implement each of the required technologies and then proceed to experiment with one or more ways to take them mobile or make it easy to do so.

---

###Mike Farr
michaelmfarr@gmail.com <br>
mikefarr@mac.com

####DBC sf-dragonflies-2015
---
<br><br><br>
###User Requirements:
* I want to use my apps via the web, my phone, my tablet and often on my PC/Mac.
* I don't want a lowest common denominator experience, each should exploit the best of it's platform
* I want my tablet and phone apps to feel like native apps
* I want my web experience to feel like a web experience when appropriate: if what I am doing is browsing and a page metaphore is appropriate, don't give me a fixed frame app.  When I resize a page of information, I want it to reflow.
* If the Internet is not available I should still have an app experience on my device using persistant data if appropriate.
 
###Developer Requirements:
* I don't want to have to write multiple separate apps
* I want to leverage MVC to keep the model and controller logic common while the view is free to change with output target
* I want to reduce the number of languages and frameworks I have to learn

###Background
In phase-1, we created several command line applications.  Taking advantage of the MVC paradigm one could swap out a vanilla command line view with something more interesting. Both my Sudoku solver and my Ruby Racer use this approach.  Here is RubyRacer (click to view video).

<a href="http://www.youtube.com/watch?feature=player_embedded&v=7eWvCm3l7pQ
" target="_blank"><img src="http://img.youtube.com/vi/7eWvCm3l7pQ/0.jpg" 
alt="Ruby Racer teaching example." width="560" height="315" border="10" /></a>

That's all well and good, but how far can this go? In the next video I replace the command-line View Module of our flashcard assignment with a RemoteView leaving the model and controller untouched.  The remote view manages a UI server I built as a native Macintosh application.  The UI server and the Ruby Flashcard app talk over sockets.  The UIServer is much like a browser except instead of HTML, it's Ruby objects that are indirectly being rendered. This is done through a RemoteView class leaving the rest of the program untouched.   
 
<a href="http://www.youtube.com/watch?feature=player_embedded&v=37ZlKUeJXfM
" target="_blank"><img src="http://img.youtube.com/vi/37ZlKUeJXfM/0.jpg" 
alt="Flashcard UI." width="560" height="315" border="10" /></a>

The next step would be to look at creating an ActiveRecord/Sinatra app, then as a native app reusing the model and controller.  


