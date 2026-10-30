# WEBSITE
The two subfolders `srv` and `httpd` are the sole folders required to host a server on a Linux device using `apache`. 

In short, the apache package handles the hosting of the server, using the configuration set in the httpd folder. 

The actual web content is stored in the srv directory.

# Instructions
To get the server running: 
- Install the "apache" package on linux (for httpd)
- Download the files
- Run "sudo Systemctl start httpd"
- Open the webpage using the url http://localhost:80 (or cilly.cat)  [note that these are defined in the /httpd/httpd.conf file, as "Listen 127.0.0.1:80" (to bind to a specific IP) and "ServerName = cilly.cat:80" (to give it a pretty name :D)

To modify the webpage, edit the contents of /srv/http.

# Folders:
## httpd
`httpd` is the service daemon used by apache (and controlled through `apachectl`: it is not suggested to invoke it directly)
note: start httpd with "sudo Systemctl start httpd"

This folder contains configuration related to actually **hosting** the server, connecting TLS, etc. including IP configuration, and it is recommended to read through the document to get a grasp of what is going on.

## srv
The `srv` directory (/srv/) is the default location for, well, server files on Linux: this path is obsolete by modern standards, and you can point `apache` to use any folder in any location.

Inside `srv`, is the `http` folder:

### http
This folder is where all the **content** of a website is to be stored: 
By default, if no page is specified, the website lands the user on `url`/`index.html`, which indexes all present `html` files. 
