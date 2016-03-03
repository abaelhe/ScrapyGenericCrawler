A crawler
=========

A crawler to collect all components together.

TODO:

* splash with HH scripts
* autologin + autoregister + login keychain
* crazy-form-submitter
* captcha solving
* pagination


Installation
------------

Requires Python 3.4:

    pip install -r requirements.lock.txt


Run crawler
-----------

Start splash:

    docker run -p 8050:8050 scrapinghub/splash

Specify url to crawl via the ``url`` param:

    scrapy crawl crawler -a url=http://127.0.0.1:8001

Useful options to tweak (add to the above command via ``-s NAME=value``):

- ``SPLASH_URL`` url of the splash instance
- ``DOWNLOAD_DELAY`` - set to 0 when crawling local test server
- ``USE_HH`` - set to 0 to disable headless-horesman scripts
