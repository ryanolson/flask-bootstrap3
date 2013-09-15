===============
Flask-Bootstrap
===============

Flask-Bootstrap packages `Twitter's Bootstrap
<http://twitter.github.com/bootstrap/>`_ into an extension that mostly consists
of a blueprint named 'bootstrap'. It can also create links to serve Bootstrap
from a CDN.

Usage
-----

Here is an example::

  from flask.ext.bootstrap import Bootstrap

  [...]

  bootstrap = Bootstrap()
  bootstrap.init_app(app)

This makes some new templates available, mainly ``bootstrap/base.html`` and
``bootstrap/base_cdn.html``. These are blank pages that include all bootstrap
resources, and have predefined blocks where you can put your content. The core
block to alter is ``body``, otherwise see the source of the template
for more possiblities.

The url-endpoint ``bootstrap.static`` is available for refering to Bootstrap
resources.::

  url_for('bootstrap.static', filename='...')

