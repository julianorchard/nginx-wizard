# Nginx Wizard

A simple but very handy Python 3 script to set up [Nginx](https://www.nginx.com/) URLs with some basic configuration files. The steps and configurations in this file are ones I found myself needing to do pretty much every time you want to add a new URL.

Tested on Ubuntu 20.04 LTS. Should work on other distributions.

## Dependencies

On Ubuntu, this command will install the right dependencies:

```sh
sudo apt install nginx certbot python3-certbot-nginx
```

Required:

- Python 3 (ships with most distros)
- Nginx

Optional:

- [Certbot](https://github.com/certbot/certbot) to create certificates for the URLs set up by this script

## Installation

Clone the repository to a location you like:

```sh
git clone https://github.com/julianorchard/nginx-wizard
```

## Usage

The process this wizard guides you through is pretty simple. It looks something like this:

```sh

$ sudo nginx-wizard/nginx-wizard

  Please enter your user account username: exampleuser
  Please enter the site URL: test.com

  Creating directory at /var/www/test.com...
  Creating a shortcut to directory in /home/exampleuser/...

  Would you like this setup to use the SSL configuration file? (y/n) n

  Moving Nginx template file into position with new details...
  Creating link from /sites-available/ to /sites-enabled/...

  Don't forget to refresh service with 'service nginx reload'!

```

## Contributing

Please submit a [pull request](https://github.com/julianorchard/nginx-wizard/pulls) or an [issue](https://github.com/julianorchard/nginx-wizard/issues).

## License

This script is under the MIT License. See the [license](/LICENSE) file for more information.
