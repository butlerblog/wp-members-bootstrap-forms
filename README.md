# wp-members-bootstrap-forms
Functions to overwrite various login, registration and other forms of the WP-Members Wordpress plugin for use with Twitter Bootstrap based themes.

The original version of this file used pluggable functions to rewrite the form display.  Rewriting functions is not a good way to approach these changes.  A better method is to use the filter hooks provided in the code to change the tags accordingly.  Interestingly, those filter hooks are actually documented right in the very function that was being edited.

I've replaced the login form function changes with the appropriate filter functions in the hopes that it might serve as an example of the preferred/correct method of making changes that will leave your application sustainable so that you can upgrade without making your changes obsolete.  Additionally, it takes what needed over 300 lines of extra code and reduces it to around 80 (including my wordy comments).

The further down the development road the plugin goes, the less likely an unmaintained pluggable function will work.  But a properbly constructed filter function should never become obsolete as long as the original hook remains in place.
