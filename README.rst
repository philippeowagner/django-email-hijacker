=====================
Django Email Hijacker
=====================

.. image:: https://travis-ci.org/OohlaLabs/django-email-hijacker.svg?branch=master
    :target: https://travis-ci.org/OohlaLabs/django-email-hijacker

.. image:: https://coveralls.io/repos/OohlaLabs/django-email-hijacker/badge.png?branch=master
    :target: https://coveralls.io/r/OohlaLabs/django-email-hijacker

Django Email Hijacker lets you send emails via your favourite email backend but sends them to a specified email address instead of the intended recipients.
It allows you to send emails via a real backend from a development or staging environment without worrying that an actual user might get sent unintended emails.


Installation
------------
::

    pip install django-email-hijacker


In your development ``settings.py``::

    EMAIL_BACKEND = "email_hijacker.backends.hijacker.EmailBackend"
    HIJACKER_EMAIL_ADDRESS = "hijacker@example.org"
    HIJACKER_EMAIL_BACKEND = "your.real.EmailBackend"


Running Tests
-------------
::

    tox


Contributions
-------------

All contributions and comments are welcome.

Change Log
----------

v0.1
~~~~
* Initial