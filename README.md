WireMailMandrill
================

This module is an extension for the WireMail class to utilise the Mandrill HTTPS API.

It includes the official Mandrill PHP API client library.




Installation
============

- Place module files inside `/site/modules/WireMailMandrill/`
- Follow the standard ProcessWire module installation method (Admin, Modules, New, Refresh, Install)
- Obtain a Mandrill API key from the logged in `Settings` page.
- View the WireMailMandrill module configuration page and enter the API key.


Usage
=====

All messaging functions throughout the site that use WireMail or wireMail() when this module is installed.


Example code
------------

```php
$mail = wireMail();

$mail->from('john.hammond@jurassicpark.com', 'John Hammond');
$mail->to('alan.grant@dinosaurfun.com', 'Alan Grant');
$mail->subject('The park is open');
$mail->bodyHTML($bodyHTML);

// Add an attachment
$mail->attachment($somePage->files->first()->filename);

$count = $mail->send();
```




Links
-----

- [Mandrill](https://mandrillapp.com/)
- [Mandrill API documentation](https://mandrillapp.com/api/docs/messages.php.html)
- [Mandrill Account Settings (API key page)](https://mandrillapp.com/settings)
- [Mandrill PHP client library](https://bitbucket.org/mailchimp/mandrill-api-php/)




Changelog
---------

### v0.0.1 2015-05-30

- Initial release, beta.




Licence
-------

GPLv2