clone Project
`git clone https://github.com/ProjectPartnersManagement/document-hash`

Change into the cloned directory

`cd document-hash`

Install JavaScript dependencies

`npm install`

Compile angular app

`npm run aot`

Install nginx 

`apt-get install nginx`

Copy the nginx configuration files from `document-hash/nginx/` to your `/etc/nginx/`.

Rename `/etc/nginx/sites-available/your-domain-name.local` to a more meaningful name. Replace the file's contents accordingly.
Add the local domain you chose to your [hosts file]

Create a symbolic link to your new configuration file so that nginx knows you want to use this config

`cd /etc/nginx/sites-enabled/ && sudo ln -s ../sites-available/your-domain-name.local`

Restart nginx

`sudo service nginx restart`

