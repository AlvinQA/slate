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
404 | Not Found -- The specified resource could not be found.
405 | Method Not Allowed -- You tried to access a resource with an invalid method.
429 | Too Many Requests -- You've made too many API requests in a short time
500 | Internal Server Error -- There was an issue on our end. Please try your request again.
503 | Service Unavailable -- The API is offline for maintenance. Please try again later.
