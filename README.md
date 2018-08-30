# SREChallange

* Create and deploy a running instance of a web server using a configuration management tool of your choice. The web server should serve one page with the following content.

```
<html>
<head>
<title>Hello World</title>
</head>
<body>
<h1>Hello World!</h1>
</body>
</html>
```

* Secure this application and host such that only appropriate ports are publicly exposed and any http requests are redirected to https. This should be automated using a configuration management tool of your choice and you should feel free to use a self-signed certificate for the web server.

* Develop and apply automated tests to validate the correctness of the server configuration.

#Roles

There are 2 roles, 1 that will provision the EC2 instance - inorder for that to work you will need to set the vars within Defaults.

The 2nd role is the actual configuration role of the EC2 instance and it will deploy HTTPS over NGINX, for that to work you will need to update the IP of the actual EC2 instance within /dev/inventory.

To run the playbook make sure to be on the root folder and run :

sudo ansible-playbook -i dev filename
