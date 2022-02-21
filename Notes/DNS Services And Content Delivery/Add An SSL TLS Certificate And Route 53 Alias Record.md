Setting up a secure certificate using SSL/TLS to have secure connections using HTTPS.

Services -> Certificate Manager (you need to be in N.Virginia region)

Provision Certificate -> Get started -> request public certificate -> type domain name -> next

Email validation -> confirm and request

You should now receive an email in your inbox

CloudFront -> check the box for your distribution -> distribution settings -> edit

- alternate domain name (cloudforbeginners.net)
- custom SSL certificate (select your certificate)
- default root object (index.html)

Click yes edit

Route 53 -> Hosted Zones -> find your hosted zone for your domain -> create record set

If you added www to your initial certificate you would add that record in here:

- name (www)
- type (A) 
- alias (yes)
- alias target (CloudFront distribution)
- routing policy (simple)

Click on create.

MAC
There is a "dig" utility that you can run in the terminal:

```
dig cloudforbeginners.net
```

Windows
```
nslookup
cloudforbeginners.net
```

This should return an indication that everything is okay in the terminal.

Then in the browser type

```
https//cloudforbeginners.net
```

And it should render the page. (In the lesson they did not add www to the certificate and add it as a record)

