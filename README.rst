==========================
Askbot-Heroku - Q&A forum
==========================

This is a fork of the Askbot project - open source Q&A system, like StackOverflow, Yahoo Answers and some others.

This fork consists of an initialized Askbot installation containing the necessary modifications to deploy in heroku with a PostgreSQL database.

To deploy in heroku:

1. Create the heroku app with ``heroku create``
2. Push to the heroku repository: ``git push heroku master``
3. Set environment variables in heroku::

   $ heroku config:set DJANGO_SETTINGS_MODULE=app.settings
   $ heroku config:set SECRET_KEY="some_random_value"

4. ``syncdb`` and ``migrate``::

   $ heroku run python ./manage.py syncdb
   $ heroku run python ./manage.py migrate

To get a value for SECRET_KEY you can use the linux utility ``apg``.

I will try to keep this repository synced with https://github.com/ASKBOT/askbot-devel.git but this is not guaranteed.

The rest of this README comes from the original project.

Demo site is http://askbot.org

All documentation is in the directory askbot/doc

Askbot is based on code of CNPROG, originally created by Mike Chen 
and Sailing Cai and some code written for OSQA
