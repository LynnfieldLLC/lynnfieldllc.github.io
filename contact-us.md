---
layout: page
title: Contact Us
permalink: /contact-us/
---
<form action="//formspree.io/lynnfield.llc@gmail.com" role="form" method="POST">
	<div class="form-group">
		<label for="name">What's your name?</label>
    	<input id="name" type="text" name="name" class="form-control">
	</div>
	
	<div class="form-group">
		<label for="name">What's your email?</label>
    	<input id="email" type="email" name="_replyto" class="form-control">
	</div>
	
	<div class="form-group">
		<label for="name">How can we help?</label>
		<textarea id="body" name="body" class="form-control" rows="8"></textarea>
	</div>
	
    <input id="submit" class="btn btn-lg" type="submit" value="Submit" disabled>
	<input type="hidden" name="_next" value="/thanks">
	<input type="text" name="_gotcha" style="display:none">
</form>

<script>
	// Hope you aren't using IE8 or earlier ;)
	document.addEventListener('DOMContentLoaded', function() {
		document.addEventListener("keyup", function() {
			var name = document.getElementById("name").value;
			var email = document.getElementById("email").value;
			var body = document.getElementById("body").value;
			
			var allFieldsValid = !!name && !!name.trim() &&
				!!email && !!email.trim() &&
				!!body && !!body.trim();
				
			document.getElementById("submit").disabled = !allFieldsValid;
		});
 	});
</script>