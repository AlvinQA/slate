# Errors

<aside class="notice">
This error section is stored in a separate file in <code>includes/_errors.md</code>. Slate allows you to optionally separate out your docs into many files...just save them to the <code>includes</code> folder and add them to the top of your <code>index.md</code>'s frontmatter. Files are included in the order listed.
</aside>

The Surveillus API uses the following error codes:


Error Code | Meaning
---------- | -------
400 | Bad Request -- There was something wrong with your request.
401 | Unauthorized -- Your API key is incorrect.
403 | Forbidden -- You do not have access to the requested resource.
404 | Not Found -- The specified kitten could not be found.
405 | Method Not Allowed -- You tried to access a method with an invalid method.
429 | Too Many Requests -- You're requesting too many kittens! Slow down!
500 | Internal Server Error -- We had a problem with our server. Try again later.
503 | Service Unavailable -- We're temporarily offline for maintenance. Please try again later.
