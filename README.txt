Module description
------------------

The Emailmanager module allows the administrator to switch the standard SMTP 
library over to use the third party Emailmanager library. An account with 
Emailmanager is required to use this module.

The recommended third party library for this module is the latest version
of the Emailmanager PHP class v0.4.4 by Markus Hedlund et al.
http://github.com/Znarkus/emailmanager-php

Note: The module uses the REST API to connect to Emailmanager.

Installation
------------

Installing the Drupal 7 version of the Emailmanager module requires a few steps :

1) Download the Mail System module into sites/all/modules, then enable it.
   http://drupal.org/project/mailsystem

2) Copy the emailmanager folder to the modules folder in your installation 
   This is usually sites/all/modules.

3) Obtain the Emailmanager PHP library from http://github.com/Znarkus/emailmanager-php.

4) Copy the files to the includes directory in the module folder
   /modules/emailmanager/includes.

5) You must ensure you get the Certificate folder too as this is now implemented
   within the PHP class.

6) Enable the module using Administer > Modules (/admin/build/modules).

7) Go to Site configuration > Emailmanager (/admin/settings/emailmanager)
   
8) Enable Emailmanager functionality and add your API key from your Emailmanager account.

9) The test functionality enables you to test the integration is working, this 
   will use a credit by default each time you submit an email address.

10) The email address that emails are sent from on your site must have a valid 
   Sender Signature set up in your Emailmanager account. Different modules use 
   different settings for the "From" address. One important place to check is 
   the address on Administer > Site configuration > Site information.
	 
11) Emails sent from the Contact module will use the sender email as the Reply To
   address, and will append the sender's email address to the bottom of the email
	 so the recipient can see who submitted the Contact form.  This is necessary
	 when using Emailmanager, as all emails must be sent from a sender defined by a
	 Sender Signature.  The "From" email address is the address defined by the
	 setting on Administer > Site configuration > Site information.

12) Configure the Mail System module (setup in step 1) so that all modules use
    Emailmanager to send email.  Alternatively, you can configure it so some modules
		use other mail modules or the default Drupal mail handler if you'd like. For
		example, if you don't like the way the Contact module is handled, you can
		set things up so Contact module emails are sent by the regular Drupal mail
		handler.

Support and bugs
----------------

If you have any problems using the module, please submit an issue in the 
Emailmanager queue (http://drupal.org/project/issues/emailmanager).

That's also a good place to check for known problems and "todos".

Credit
------

The Emailmanager module was developed by
 * Luke Simmons (luketsimmons)
 * Allister Price (alli.price)
from Deeson Online (http://www.deeson.co.uk/online).

Credit also goes to the phpmailer (http://drupal.org/project/phpmailer) module on 
which this module is heavily based.
