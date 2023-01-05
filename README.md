# Nginx Wizard 🧙‍♂️

A [Python](https://www.python.org/) script to configure new URLs on [Nginx](https://www.nginx.com/), via a [command line](https://en.wikipedia.org/wiki/Command-line_interface) [wizard](https://en.wikipedia.org/wiki/Wizard_(software)). 

The steps and configurations chosen are those I found myself needing the most when adding new URLs.

Tested on [Ubuntu 20.04 LTS](https://releases.ubuntu.com/focal/). Should work on other distributions.

## Dependencies

Required:

- Python 3
- Nginx

Optional:

- [Certbot](https://github.com/certbot/certbot) to create certificates for the URLs set up by this script

### Debian/Ubuntu

If using [APT](https://wiki.debian.org/Apt), the following command will install the right dependencies:

```sh
sudo apt install nginx certbot python3-certbot-nginx
```

## Installation

Clone the repository to a location you like (*ideally* somewhere in your PATH):

```sh
git clone https://github.com/julianorchard/nginx-wizard
```

## Usage

The process this wizard guides you through is pretty simple. 

It looks something like this:

```txt

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

If something needs fixing, please submit a [pull request](https://github.com/julianorchard/nginx-wizard/pulls) or an [issue](https://github.com/julianorchard/nginx-wizard/issues). If there is a configuration you would like to change, it *might* be best to fork this repository and work on your own changes: the changes you want to implement might be personal preference! 

However, if there is a change which you think would be a better default, please contact with me [via email](mailto:jorchard@pm.me) or [@jdo@mastodon.social](https://mastodon.social/@jdo)!

## License

The contents of this repository is under the MIT License. Please see the [license](/LICENSE) file for more information.
