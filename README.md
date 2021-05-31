# htpw

.htaccess to protect Wordpress



### Description

*htpw* is a project to increase the security of your Wordpress installation without installing external plugins to preserve memory, space and integrity of the cms installation.

It doesn't introduce invasive rules (XSS or Injection protection) to avoid creating malfunctions with external plugins.



### Functionality

*htpw* introduces protection against:

- Protect log files;
- Protect system files;
- Disable directory listening;
- Implementation of Security Headers;
- Block malicious or suspicious user agent;
- Disable the execution of PHP code in the Upload directory;
- Disable the execution of PHP code in the Plugins directory (rule by default disabled);
- Disable the execution of PHP code in the Themes directory;
- Block XML-RPC requests except JetPack or Akismet connections.



### Installation

Add to the bottom of your .htaccess file the contents of the [htaccess](https://github.com/drego85/htpw/blob/main/htaccess) file.

*htpw* works if your webserver is Apache (not NGINX).



### Testing

If you want to test if the new rules work and protect your Wordpress site you can use WPScan (WordPress Security Scanner), if the default scan fails *htpw* is working!

You can install WPScan on your PC or use it [online](https://w-e-b.site/?act=wpscan&color=on), online scan failed example:


![WPScan Fails via htpw](https://pbs.twimg.com/media/EvD-mSpWYAIEjrD?format=png&name=small)



### Credits

* [Andrea Draghetti](https://twitter.com/AndreaDraghetti) is the creator of the project;
* [iThemes Security](https://wordpress.org/plugins/better-wp-security/) for some htaccess rules.



### License

GNU General Public License v3.0
