# Simple-CSRF-Prevention-1
implementing Cross-site Request Forgery protection in web applications via Synchronizer Token Patterns 

This web app is a demonstration of how to prevent CSRF with a Synchronizer Token Patterns. How it happens is, when a POST request is made to the server it should contain a CSRF token previously fetched by an AJAX request. At the point of validation, serer side cide compares this token with the token stored in the session memory. If it matches, it'll be safe to process the data. This way prevents malicious CSRF attacks.

This demonstration has 3 files in it. the index.php file contains the login form and the validation code for the login. At the point of login, it creates a CSRF token saves in the server side. The protected.php file contains the are protected by the login, which is a contact form. When the page loads, a javascript code calls the server via AJAX to get the CSRF token and adds it into a hidden field in the form. The get-token.php file is the endpoint that gives the Token to the AJAX request.
