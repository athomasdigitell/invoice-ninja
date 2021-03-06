# Invoice Ninja
## Simple, Intuitive Invoicing

### [https://www.invoiceninja.com](https://www.invoiceninja.com)

#### Note: please submit any pull requests against the [Laravel 5](https://github.com/hillelcoren/invoice-ninja/tree/laravel-5) branch

If you'd like to use our code to sell your own invoicing app we have an affiliate program. Get in touch for more details.

### Introduction

Most online invoicing sites are expensive. They shouldn't be. The aim of this project is to provide a free, open-source alternative. Additionally, the hope is the codebase will serve as a sample site for Laravel as well as other JavaScript technologies.

To setup the site you can either use this [zip file](https://www.invoiceninja.com/knowledgebase/self-host/) (easier to setup) or checkout the code from GitHub following the instructions below (easier to stay up to date).

For a WAMP/MAMP/LAMP setup you can one-click install using Softaculous's [AMPPS](http://www.ampps.com/). To deploy the app with [Docker](http://www.docker.com/) you can use [this project](https://github.com/rollbrettler/Dockerfiles/tree/master/invoice-ninja).

To connect follow [@invoiceninja](https://twitter.com/invoiceninja) or join the [Facebook Group](https://www.facebook.com/invoiceninja). For discussion of the code please use the [Google Group](https://groups.google.com/d/forum/invoiceninja).

If you'd like to translate the site please use [caouecs/Laravel4-long](https://github.com/caouecs/Laravel4-lang) for the starter files.

Developed by [@hillelcoren](https://twitter.com/hillelcoren) | Designed by [kantorp-wegl.in](http://kantorp-wegl.in/).

### Features

* Core application built using Laravel 4.1
* Invoice PDF generation directly in the browser
* Integrates with many payment providers
* Recurring invoices
* Tax rates and payment terms
* Multi-user support
* [Zapier](https://zapier.com/) integration
* [D3.js](http://d3js.org/) visualizations

### Contributors

* [Troels Liebe Bentsen](https://github.com/tlbdk)
* [Jeramy Simpson](https://github.com/JeramyMywork) - [MyWork](https://www.mywork.com.au)

### Documentation 

* [Self Host](https://www.invoiceninja.com/knowledgebase/self-host/)
* [API Documentation](https://www.invoiceninja.com/knowledgebase/api-documentation/)
* [Developer Guide](https://www.invoiceninja.com/knowledgebase/developer-guide/)

### Steps to setup from GitHub

If you plan on submitting changes it's best to [fork the repo](https://help.github.com/articles/fork-a-repo), otherwise you can just checkout the code.

    git clone https://github.com/hillelcoren/invoice-ninja.git ninja
    cd ninja

Install Laravel packages using Composer

Note: you may be prompted for your Github user/pass due to their API limits. 

    composer install

Install JavaScript and HTML packages using Bower. This is optional, it's only needed if you want to modify the JavaScript.

    bower install

Create database user and a database for ninja

    CREATE SCHEMA `ninja` DEFAULT CHARACTER SET utf8 COLLATE utf8_general_ci;
    CREATE USER 'ninja'@'localhost' IDENTIFIED BY 'ninja';
    GRANT ALL PRIVILEGES ON `ninja`.* TO 'ninja'@'localhost';
    FLUSH PRIVILEGES;

Add public/ to your web server root then load / to configure the application.

### Developer Notes

* The application requires PHP >= 5.4.0
* If you make any changes to the JavaScript files you need to run grunt to create the built files. See Gruntfile.js for more details.
* The lookup tables are cached in memory (ie, Currencies, Timezones, Languages, etc). If you add a record to the database you need to clear the cache by uncommenting Cache::flush() in app/routes.php.
* If you run into any composer errors try running composer dump-autoload. 

### Ubuntu Notes

    # Install php-mcrypt
    apt-get install php5-mcrypt
    sudo php5enmod mcrypt

    # Install Composer
    curl -sS https://getcomposer.org/installer | php
    sudo mv composer.phar /usr/local/bin/composer

    # Install Bower
    sudo apt-get install npm nodejs-legacy
    sudo npm install -g bower
    sudo ln -s /usr/local/lib/node_modules/bower/bin/bower /usr/local/bin/bower

    # Install Grunt (For development only)
    npm install -g grunt-cli

### Frameworks/Libraries
* [laravel/laravel](https://github.com/laravel/laravel) - A PHP Framework For Web Artisans
* [twbs/bootstrap](https://github.com/twbs/bootstrap) - Sleek, intuitive, and powerful front-end framework for faster and easier web development.
* [patricktalmadge/bootstrapper](https://github.com/patricktalmadge/bootstrapper) - Laravel Twitter Bootstrap Bundle
* [danielfarrell/bootstrap-combobox](https://github.com/danielfarrell/bootstrap-combobox) - A combobox plugin 
* [jquery/jquery](https://github.com/jquery/jquery) - jQuery JavaScript Library
* [eternicode/bootstrap-datepicker](https://github.com/eternicode/bootstrap-datepicker) - A datepicker for @twitter bootstrap
* [jquery/jquery-ui](https://github.com/jquery/jquery-ui) - The official jQuery user interface library
* [knockout/knockout](https://github.com/knockout/knockout) - Knockout makes it easier to create rich, responsive UIs with JavaScript
* [rniemeyer/knockout-sortable](https://github.com/rniemeyer/knockout-sortable) - A Knockout.js binding to connect observableArrays with jQuery UI sortable functionality
* [MrRio/jsPDF](https://github.com/MrRio/jsPDF) - Generate PDF files in JavaScript. HTML5 FTW.
* [FortAwesome/Font-Awesome](https://github.com/FortAwesome/Font-Awesome) - The iconic font designed for Bootstrap that works with twitter bootstrap
* [jasonlewis/basset](https://github.com/jasonlewis/basset) - A better asset management package for Laravel
* [Zizaco/confide](https://github.com/Zizaco/confide) - Confide is a authentication solution for Laravel 4
* [Anahkiasen/former](https://github.com/Anahkiasen/former) - A powerful form builder, for Laravel and other frameworks (stand-alone too)
* [barryvdh/laravel-debugbar](https://github.com/barryvdh/laravel-debugbar) - Laravel debugbar
* [DataTables/DataTables](https://github.com/DataTables/DataTables) - Tables plug-in for jQuery
* [Chumper/Datatable](https://github.com/Chumper/Datatable) - This is a laravel 4 package for the server and client side of datatables
* [omnipay/omnipay](https://github.com/omnipay/omnipay) - A framework agnostic, multi-gateway payment processing library for PHP 5.3+
* [Intervention/image](https://github.com/Intervention/image) - PHP Image Manipulation
* [webpatser/laravel-countries](https://github.com/webpatser/laravel-countries) - Almost ISO 3166_2, 3166_3, currency, Capital and more for all countries
* [briannesbitt/Carbon](https://github.com/briannesbitt/Carbon) - A simple API extension for DateTime with PHP 5.3+
* [thomaspark/bootswatch](https://github.com/thomaspark/bootswatch) - Themes for Bootstrap
* [mozilla/pdf.js](https://github.com/mozilla/pdf.js) - PDF Reader in JavaScript
* [nnnick/Chart.js](https://github.com/nnnick/Chart.js) - Simple HTML5 Charts using the canvas tag
* [josscrowcroft/accounting.js](https://github.com/josscrowcroft/accounting.js) - A lightweight JavaScript library for number, money and currency formatting
* [jashkenas/underscore](https://github.com/jashkenas/underscore) - JavaScript's utility _ belt 
* [caouecs/Laravel4-long](https://github.com/caouecs/Laravel4-lang) - List of languages ​​for Laravel4
* [calvinfroedge/PHP-Payments](https://github.com/calvinfroedge/PHP-Payments) - A uniform payments interface for PHP
* [bgrins/spectrum](https://github.com/bgrins/spectrum) - The No Hassle JavaScript Colorpicker
* [lokesh/lightbox2](https://github.com/lokesh/lightbox2/) - The original lightbox script
