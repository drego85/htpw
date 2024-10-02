# htpw - Htaccess To Protect WordPress

*htpw* (Htaccess To Protect WordPress) is a project designed to improve the security of your WordPress installation by leveraging `.htaccess` rules, without the need for external plugins. This approach helps maintain system resources while ensuring compatibility with your existing setup.

### Features

*htpw* enhances security through the following measures:

- **Log Files Protection**: Prevents unauthorized access to log files.
- **System Files Protection**: Secures critical WordPress system files such as `.htaccess`, `wp-config.php`, and others.
- **Disable Directory Listing**: Prevents visitors from viewing directory contents.
- **Security Headers Implementation**: Adds essential HTTP headers to enhance your website's security.
- **User-Agent Blocking**: Blocks malicious or suspicious user agents.
- **Disable PHP Execution in Uploads Directory**: Prevents execution of PHP files in the `wp-content/uploads` directory.
- **Disable PHP Execution in Plugins Directory (optional)**: Optionally blocks PHP execution in the plugins directory.
- **Disable PHP Execution in Themes Directory (optional)**: Optionally blocks PHP execution in the themes directory.
- **Block XML-RPC Requests (except JetPack and Akismet)**: Restricts XML-RPC requests to only trusted services.

### Why Use htpw?

WordPress, being one of the most popular content management systems, is often targeted by attackers. While there are many security plugins available, they can sometimes consume significant resources or cause compatibility issues. *htpw* provides a lightweight alternative by integrating security rules directly into the `.htaccess` file, ensuring:

- Efficient protection with minimal resource usage.
- Reduced risk of conflicts with themes and plugins.
- Simple installation and configuration.
- Direct control over security measures without relying on external plugins.

### Installation

To install *htpw*:

1. Download the `.htaccess` file from the [GitHub repository](https://github.com/drego85/htpw/blob/main/htaccess).
2. Add the contents of the `.htaccess` file to the bottom of your existing `.htaccess` file in your WordPress installation.
3. Ensure your web server is running Apache (this configuration is not compatible with NGINX).

For users with a CDN (e.g., Cloudflare), it’s recommended to install the `mod_remoteip` Apache module to ensure correct IP address logging.

### Testing

You can test if the *htpw* rules are working properly by using [WPScan](https://wpscan.com/), a WordPress Security Scanner. If the default scan is blocked, then *htpw* is functioning as expected.

Alternatively, you can test online using services like this [online scanner](https://w-e-b.site/?act=wpscan&color=on). Here's an example of WPScan being blocked by *htpw*:

![WPScan Block Example](https://pbs.twimg.com/media/EvD-mSpWYAIEjrD?format=png&name=small)

### Troubleshooting

- **CDN Compatibility**: If you're using a CDN such as Cloudflare, ensure that the `mod_remoteip` module is installed on your Apache server to correctly log visitor IP addresses.
- **Plugin Conflicts**: Some plugins that use XML-RPC may require additional configuration to work correctly. Ensure trusted services like JetPack or Akismet are allowed through the XML-RPC restrictions.

### Customization

*htpw* can be customized to fit your specific security needs:

- **Disable PHP Execution in Themes/Plugins**: By default, PHP execution is allowed in the themes and plugins directories. You can modify the `.htaccess` rules to disable this for added security.
  
- **Additional Security Headers**: You may wish to add further security headers, such as `Content-Security-Policy` or `Permissions-Policy`, depending on the specific needs of your website.

### Contributing and Supporting the Project

There are two ways you can contribute to the development of **Tosint**:

1. **Development Contributions**:

   Please ensure that your code follows best practices and includes relevant tests.

2. **Donation Support**:
   If you find this project useful and would like to support its development, you can also make a donation via [Buy Me a Coffee](https://buymeacoffee.com/andreadraghetti). Your support is greatly appreciated and helps to keep this project going!

   [![Buy Me a Coffee](https://img.shields.io/badge/-Buy%20Me%20a%20Coffee-orange?logo=buy-me-a-coffee&logoColor=white&style=flat-square)](https://buymeacoffee.com/andreadraghetti)

### License

This project is licensed under the GNU General Public License v3.0.