===========================================================
Collect debugging information from live Odoo server Sentry
===========================================================

savoirfairelinux.com

Sentry
------

getsentry.com

realtime event logging and aggregation
monitor errors 
aggregate information -> postmortem

odoo implementation
--------------------

patch http.py, intercept exception, send them to sentry

-> nice

currently does not handle crons

look at Raven (check what this does)

cgtb: standard addon

currently catches unhandled exceptions

possible to create events on ERROR log messages 
