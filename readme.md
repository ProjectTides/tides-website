# Tides website installation guide

## Prerequisites

1. Composer
2. NPM
3. Grunt

## Installation

1. Fork the master repository. [Know more on how to **fork a repo**](https://help.github.com/articles/fork-a-repo/)

   * Create a local clone for the forked repository.

   * Avoid creating a sync with the master repository.

2. On your local machine, Run `composer install` in the root directory using the CLI.

3. Run `npm install` on */wp-content/themes/tides/* directory. We are using `tides` as default theme.

4. Run `grunt` to check if the grunt installation worked. You should see a style.css and main.js inside your theme. 

5. Secure your WordPress installation.

   * Rename `wp-sample-config.php` to `wp-config.php`.

   * [Generate](https://api.wordpress.org/secret-key/1.1/salt/) a new set of auth keys. 

   * Replace the auth key code in wp-config.php with newly generated set of auth keys.
      ```
  
      define('AUTH_KEY', '');
  
      define('SECURE_AUTH_KEY', '');
  
      define('LOGGED_IN_KEY', '');
  
      define('NONCE_KEY', '');
  
      define('AUTH_SALT', '');
  
      define('SECURE_AUTH_SALT', '');
  
      define('LOGGED_IN_SALT', '');
  
      define('NONCE_SALT', '');
  
      ```

   * Change the table prefix as you need in `wp-config.php`.
   

6. Configure the database.

   * Create a new MySql database for tides website.

   * Update configurations for newly created database in `wp-config.php`.
      ```
      define('DB_NAME', '');
      
      define('DB_USER', '');
      
      define('DB_PASSWORD', '');
      
      define('DB_HOST', '');
      
      define('DB_CHARSET', 'utf8');
      
      ```
