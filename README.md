Dropwizard Papertrail
=====================

Addon for Dropwizard adding support for logging to [Papertrail](https://papertrailapp.com).

Important: This addon only supports sending data to papertrail over TLS. If you need insecure communication this plugin is not for you.


Usage
-----

The Dropwizard Papertrail addon provides an `AppenderFactory` which is automatically registered in Dropwizard and will send log messages directly to Papertrail.


Configuration
-------------

A typical configuration looks like this

    appenders:
      - type: console
      - type: papertrail
        host: XXXX.papertrailapp.com
        port: 22222
        ident: my-identifier
        # timezone: UTC
        # facility: USER
        # sendLocalName: true


Properties
----------

* **host**: The URL provided by papertrail where you should log to;
* **port**: The port provided by papertrail where you should log to;
* **ident**: The identifier of your application;
* **timezone**: The timezone for logs. Defaults to *UTC*;
* **facility**: The syslog facility. Defaults to *USER*;
* **sendLocalName**: If the local name of the server should also be sent. Defaults to *true* ;




License
-------

Copyright (c) 2014 dc-square GmbH

This library is licensed under the Apache License, Version 2.0.

See http://www.apache.org/licenses/LICENSE-2.0.html or the LICENSE file in this repository for the full license text.