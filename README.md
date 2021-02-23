# htpw

.htaccess to protect Wordpress



### Description

htpw is a project to increase the security of your Wordpress installation without installing external plugins to preserve memory, space and integrity of the cms installation.

It doesn't introduce invasive rules (XSS or Injection protection) to avoid creating malfunctions with external plugins.



### Functionality

htpw introduces protection against:

- Protect system files;
- Disable directory listening;
- Disable the execution of PHP code in the Upload directory;
- Disable the execution of PHP code in the Plugins directory;
- Disable the execution of PHP code in the Themes directory;
- Block malicious or suspicious user agent;
- Block XML-RPC requests except JetPack or Akismet connections.



### Installation

Add to the bottom of your .htaccess file the contents of the [htaccess](https://github.com/drego85/htpw/blob/main/htaccess) file. 

### Credits

* [Andrea Draghetti](https://twitter.com/AndreaDraghetti) is the creator of the project;
* [iThemes Security](https://wordpress.org/plugins/better-wp-security/) for some htaccess rules.



### License

GNU General Public License v3.0
