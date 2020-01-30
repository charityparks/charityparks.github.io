---
layout: post
title:      "Params!...say again? "
date:       2020-01-30 16:37:33 -0500
permalink:  params_say_again
---

"Params" has been somewhat confusing to me for a while and I've noticed this can be very common  amongst newbies.  I felt like I wasn't really finding an answer that made it clear as to what params meant.  So this has sparked a deeper-dive into the subject for me.  Let me explain 'params' as best I can.

Params come in the form of a hash.  The params hash is a collection of data that has come through application in a request.  A hash is a series of key-value pairs. Both the key and the value are strings.   The 'key' of the key-value pair is the name.  The 'value' of the key-value pair is the content.  An example would be...the key might be 'color', and the value might be 'blue'.

Example:  colors = {"color" => "blue"}

Params values can be accessed from a GET request query, or in the form data of a POST request.  And lastly a params value can come from the path of a url.

Example:  get '/photo/:id'... then the request to a URL like this:  http://charitysphotos.cm/photos/13 .. this will set 
params[:id] to 13.

Example:  

<h1>Add a Podcast</h1>

<form action="/podcasts" method="post">
<br>
<label>Podcast Name:</label>
<input type="text" name="name">

<label>Host:</label>
<input type="text" name="host">
<br>
<button type="submit">Add Podcast</button>

</form>

The params this form creates are the podcast[name] and podcast[host]

In conclusion, params is a hash that Sinatra has made available so that you can use the in your routes and it will include the data you've requested.

