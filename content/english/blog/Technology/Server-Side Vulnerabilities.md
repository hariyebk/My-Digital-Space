---
title: "Understanding Common Types of Server-Side Vulnerabilities"
meta_title: "Application security"
description: "A Developer's Guide for Server-Side Vulnerabilities "
date: 2024-04-24T04:08:00Z
image: "/images/security.png"
categories: ["Technology"]
author: "Harun Bekri"
tags: ["Security", "Vulnerabilities"]
draft: false
---

As much as we strive to implement new features and optimize performance for our applications, we must acknowledge that neglecting security in the development process can have severe consequences.

<hr>


In our fast-paced development environments, where time is often a scarce resource, it's all too common for security considerations to take a back seat. We find ourselves in a rush to meet deadlines, deliver new features, and enhance the user experience. However, this hurried approach, which prioritizes speed and performance over security, is fundamentally flawed. the recent incident on Commercial Bank of Ethiopia should serve as a wake-up call.The stakes involved when the security of an application is flawed are significant and extend far beyond financial implications. They encompass the trust and confidence of our users, the reputation of our organizations, and the potential for legal and regulatory consequences. In this blog post, we will explore some of the most prevalent server-side vulnerabilities that developers should be aware of. From Sql injection attacks to authentication flaws, we will delve into the inner workings of these vulnerabilities and their potential impact.

<br>

##### 1. Path Traversal


 Path Traversal Vulnerabilities happen when a code queries a filename like an image from a specific route like `/images?filename=logo.png`. The file reader Api on the server can then locate the file. using this vulnerability we can can easily access other files hosted on the server by changing the filename in the query string into a path like `../../../etc/passwd` , which allows us to access the root directory.

<br>

##### 2. Vertical privilege escalation


VPE vulnerabilities occurs when there is unprotected admin functionalities like an admin page. the admin Pannal URL can be found in `robots.txt` file, or it can be imbedded inside a JavaScript file  or the `/admin` route might not be protected at all. if we got access to the admin page in a web application,  We have escalated our privilege to become an admin . the URL can sometimes be unpredictable or might be hidden in unpredictable locations. Some applications determine the user's access rights or role at login, and then store this information in a user-controllable location like a hidden field or a cookie or a query string. if this is the case , we can easily modify the role and login as an admin. 

<br>

##### 3. Horizontal privilege escalation

 HPE vulnerabilities occurs if a user is able to gain access to resources belonging to another user, instead of their own resources of that type. For example, if an employee can access the records of other employees as well as their own, then this is horizontal privilege escalation. Horizontal privilege escalation attacks may use similar types of exploit methods to vertical privilege escalation. For example, a user might access their own account page using the following URL: `https://insecure-website.com/myaccount?id=123` . If we modified the `id` parameter value to that of another user, we might gain access to another user's account page, and the associated data and functions. In some applications, the exploitable parameter does not have a predictable value. For example, instead of an incrementing number, an application might use globally unique identifiers (GUIDs) to identify users. This may prevent an attacker from guessing or predicting another user's identifier. However, the GUIDs belonging to other users might be disclosed elsewhere in the application where users are referenced, such as user messages or reviews. Often, a horizontal privilege escalation attack can be turned into a vertical privilege escalation, by compromising a more privileged user. 

<br>

 ##### 4. Username enumeration
 
 Authentication vulnerabilities can allow us to gain access to sensitive data and functionality. They also expose additional attack surface for further exploits.  Username enumeration is when we are able to observe changes in the website's behavior in order to identify whether a given username is valid. Username enumeration typically occurs either on the login page, for example, when you enter a valid username but an incorrect password, or on registration forms when you enter a username that is already taken. This greatly reduces the time and effort required to brute-force a login because we already know that the username is valid. During a brute-force attack, the returned HTTP status code is likely to be the same for the vast majority of guesses because most of them will be wrong. If a guess returns a different status code, this is a strong indication that the username was correct. It is best practice for websites to always return the same status code regardless of the outcome, but this practice is not always followed. Sometimes the returned error message is different depending on whether both the username AND password are incorrect or only the password was incorrect.

 <br>

 
 ##### 5. Two-factor authentication
 
 If the user is first prompted to enter a password, and then prompted to enter a verification code on a separate page, the user is effectively in a "logged in" state before they have entered the verification code. In this case, it is worth testing to see if you can directly skip to "logged-in only" pages after completing the first authentication step. Occasionally, you will find that a website doesn't actually check whether or not you completed the second step before loading the page.

 <br>

 ##### 6. Server-side request forgery (SSRF)
 
 Is a web security vulnerability that allows an attacker to cause the server-side application to make requests to an unintended location. In a typical SSRF attack, the attacker might cause the server to make a connection to internal-only services within the organization's infrastructure which allows the attacker to access those services through the exploited application . In other cases, they may be able to force the server to connect to arbitrary external systems. This could leak sensitive data, such as authorization credentials. For example, let's say there's a shopping application that checks the stock availability of items in different stores through Specific API endpoint. When a user wants to view the stock status, their browser sends a request to the application, including the URL of the store. The server then makes a request to the endpoint, retrieves the stock information, and shows it to the user. In an SSRF attack, the attacker can modify the request to make it point to a localhost on the server itself. For instance, instead of the original URL, they replace it with a URL like `http://localhost/admin`. The application then fetches the contents of the `/admin` URL and returns it to the user.
 
  Normally, the `/admin` URL on the server is only accessible to authenticated users with administrative privileges. However, when the request comes from the local hosted application on port 443, the server might assume it's a trusted request and grants full access to the administrative functionality, bypassing normal access controls. granting the attacker full control over the server. In some cases the attacker can leverage the SSRF vulnerability to make a request to the URL of the router's configuration page at `http://192.168.1.1` or the default gateway's address. Since the server hosting the application is making the request from within the internal network, it can reach the router's configuration page and other Internal services and cause a lot of problems.


  <br> 


  ##### 7. file upload vulnerabilities
  
   File upload vulnerabilities arise when a web server allows users to upload files to its filesystem without sufficiently validating things like their name, type, contents, or size. Failing to properly enforce restrictions on these could mean that even a basic image upload function can be used to upload arbitrary and potentially dangerous files instead. This could even include server-side script files that enable remote code execution. In some cases, the act of uploading the file is in itself enough to cause damage. Other attacks may involve a follow-up HTTP request for the file, typically to trigger its execution by the server. From a security perspective, the worst possible scenario is when a website allows you to upload server-side scripts, such as PHP, Java, or Python files, and is also configured to execute them as code. This makes it trivial to create your own web shell on the server. A web shell is a malicious script that enables you to execute arbitrary commands on a remote web server simply by sending HTTP requests to the right endpoint. If you're able to successfully upload a web shell, you effectively have full control over the server. This means you can read and write arbitrary files, exfiltrate sensitive data, even use the server to pivot attacks against both internal infrastructure and other servers outside the network.  For example, the following PHP one-liner could be used to read arbitrary files from the server's filesystem:

	`<?php echo file_get_contents('/path/to/target/file'); ?>`  
    
    Once uploaded, sending a request for this malicious file will return the target file's contents in the response.


   In the wild, it's unlikely that you'll find a website that has no protection against file upload attacks like we saw in the above. But just because defenses are in place, that doesn't mean that they're robust. You can still exploit flaws in these mechanisms to obtain a web shell for remote code execution. One way that websites may attempt to validate file uploads is to check that the input-specific `Content-Type` header matches an expected MIME type. If the server is only expecting image files, for example, it may only allow types like `image/jpeg` and `image/png`. Problems can arise when the value of this header is implicitly trusted by the server. If no further validation is performed to check whether the contents of the file actually match the supposed MIME type, this defense can be easily bypassed using tools like Burp Repeater.

<br>

 ##### 8. OS command injection   

also known as shell injection, allows an attacker to execute operating system (OS) commands on the server that is running an application, and typically fully compromise the application and its data. Often, an attacker can leverage an OS command injection vulnerability to compromise other parts of the hosting infrastructure, and exploit trust relationships to pivot the attack to other systems within the organization. this type of Vulnerability occurs when an application Instead of directly querying a database or using a secure method to retrieve the data, it relies on a legacy system that executes a shell command which will then return the data. the request parameter the application uses from the URI can be easily modified to inject an arbitrary command. the command will get executed on the server and potentially the attacker has full control over the server.

<br>

##### 10. SQL injection  

Sqli allows an attacker to interfere with the queries that an application makes to its database. This can allow an attacker to view data that they are not normally able to retrieve. This might include data that belongs to other users, or any other data that the application can access. In many cases, an attacker can modify or delete this data, causing persistent changes to the application's content or behavior. In some situations, an attacker can escalate a SQL injection attack to compromise the underlying server or other back-end infrastructure. It can also enable them to perform denial-of-service attacks. 

- Retrieving hidden data

	Imagine a shopping application that displays products in different categories. When the user clicks on the **Gifts** category, their browser requests the URL:  `https://insecure-website.com/products?category=Gifts` This causes the application to make a SQL query to retrieve details of the relevant products from the database:  
    
        SELECT * FROM products WHERE category = 'Gifts' AND released = 1

	This SQL query asks the database to return:

		- all details (`*`)
		- from the `products` table
		- where the `category` is `Gifts`
		- and `released` is `1`.
	
	The restriction `released = 1` might be used to hide products that are not released. We could assume for unreleased products, `released = 0` .   This application doesn't implement any defenses against SQL injection attacks. This means an attacker can construct the following attack, for example: `https://insecure-website.com/products?category=Gifts'--`
	This results in the SQL query:  
    
        SELECT * FROM products WHERE category = 'Gifts'--' AND released = 1

	Crucially, note that `--` is a comment indicator in SQL. This means that the rest of the query is interpreted as a comment, effectively removing it. In this example, the query no longer includes `AND released = 1`. As a result, all products are displayed, including those that are not released yet. You can use a similar attack to cause the application to display all the products in any category, including categories that they don't know about: `https://insecure-website.com/products?category=Gifts'+OR+1=1--` This results in the SQL query:
	
	    SELECT * FROM products WHERE category = 'Gifts' OR 1=1--' AND released = 1
	
	The modified query returns all items where either the `category` is `Gifts`, or `1` is equal to `1`. As `1=1` is always true, the query returns all items.

    <br>

- Login bypass

     Imagine an application that lets users log in with a username and password. If a user submits the username `abebe` and the password `abebebesobela`, the application checks the credentials by performing the following SQL query:

	    SELECT * FROM users WHERE username = 'abebe' AND password = 'abebebesobela'
	
	In this case, an attacker can log in as any user without the need for a password. They can do this using the SQL comment sequence `--` to remove the password check from the `WHERE` clause of the query. For example, submitting the username `administrator'--` and a blank password results in the following query:

	    SELECT * FROM users WHERE username = 'administrator'--' AND password = ''

	  This query returns the user whose `username` is `administrator` and successfully logs the attacker in as that user.


<br>

Thank you for taking the time to read this blog post in its entirety.

