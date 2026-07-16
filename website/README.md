# WEBSITE
The two subfolders `srv` and `httpd` are the sole folders required to host a server on a Linux device using `apache`. 

## httpd
`httpd` is the service daemon used by apache (and controlled through `apachectl`: it is not suggested to invoke it directly)

This folder contains configuration related to actually **hosting** the server, connecting TLS, etc.

## srv
The `srv` directory (/srv/) is the default location for, well, server files on Linux: this path is obsolete by modern standards, and you can point `apache` to use any folder in any location.

Inside `srv`, is the `http` folder:

### http
This folder is where all the **content** of a website is to be stored: 
By default, if no page is specified, the website lands the user on `url`/`index.html`, which indexes all present `html` files. 
