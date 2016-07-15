---
title: Wait until all ajax requests are done
categories: []
tags: [ajax]
published: True
summary: Wait until

---

During some code review with my teammate we tackled a code where we wanted to call some method only after two asynchronous calls finished processing.  

Doing it with jQuery is pretty simple, jQuery has the [when function](http://api.jquery.com/jQuery.when/) and you can use it like this:  
{% highlight javascript linenos %}

    $.when(ajax1(),ajax2()).done(function(a1, a2){
	    console.log("ajax1() and ajax2() finished"});  
{% endhighlight %}

  

Where ajax1 and ajax2 functions returns [Deferred](http://api.jquery.com/category/deferred-object/)  object:  
{% highlight javascript linenos %}

	function ajax1(){
		return $.ajax({
		    type: 'GET',
		    url: 'index.html'
		}).done(function(){ console.log("index.html"); });
	}
	   
	function ajax2(){
		return $.ajax({
			type: 'GET',
			url: 'about.html'
		}).done(function(){ console.log("about.html"); });
	}  
{% endhighlight %}
	 
Running it will output (first and second lines can change places):  


    index.html  
    about.html  
    ajax1() and ajax2() finished

There is some other way to implement it with vanilla javascript  - using the Promise object (ES6 feature - available on Chrome 43)  
{% highlight javascript linenos %}

    var oPromise1 = new Promise(
	function(resolve, reject) {
		$.ajax({type: 'GET', url:'index.html'}).done(
			function(data, message) {
				resolve(message);
			});
		});
	
	var oPromise2 = new Promise(
	function(resolve, reject) {
		$.ajax({type: 'GET', url:'index.html'}).done(
			function(data, message) {
				resolve(message);
			});
		});
	
	Promise.all([oPromise1, oPromise2]).
	then(function(a){
		console.log(a); 
	});  
{% endhighlight %}
		
	       


