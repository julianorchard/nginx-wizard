# Apache/Nginx Wizard

A simple but very handy Python 3 script to set up [Apache](https://httpd.apache.org/) and [Nginx](https://www.nginx.com/) URLs with some basic
configuration files. The steps and configurations in this file are ones I found
myself needing to do every time I configured a new URL, so I decided to write
a script to make it more straightforward.

Only tested on Ubuntu 20.04 LTS, but should work on other distributions.

## Dependencies

On Ubuntu, this command will install the right
dependencies:

```sh
sudo apt install apache certbot python3-certbot-apache
# OR
sudo apt install nginx certbot python3-certbot-nginx
```

Required:

- Python 3 (ships with most distros)
- Apache | Nginx

Optional:

- [Certbot](https://github.com/certbot/certbot) to
create certificates for the URLs set up by this
script

## Installation

Clone the repository to a location you like:

```sh
git clone https://github.com/julianorchard/apache-nginx-wizard
```

## Usage

The process this wizard guides you through is
pretty simple. It looks something like this:

```sh
$ exampleuser @ server > sudo apache-nginx-wizard/apache-nginx-wizard

Please enter your user account username: exampleuser
Please enter the site URL: test.com

Creating directory at /var/www/test.com...
Creating a shortcut to directory in /home/exampleuser/...

Would you like this setup to use the SSL configuration file? (y/n) n

Moving Nginx template file into position with new details...
Creating link from /sites-available/ to /sites-enabled/...

Don't forget to refresh service with 'service apache|nginx reload'!
```

## Support

Please [get in touch](mailto:hello@julianorchard.co.uk) with me if you want
help with this script, or submit an issue.

