========
jobvite
=========

**This package is forked from: https://github.com/mozilla/django-jobvite**
jobvite is a `Django`_ application that provides a friendly interface to
Jobvite.

.. _Django: http://www.djangoproject.com/

Installation
------------
Fetch django-jobvite::

  

Add ``django_jobvite`` to ``INSTALLED_APPS`` in ``settings.py``: ::

   INSTALLED_APPS = (
       ...
       'jobvite',
       ...
   )

Configure ``urls.py``: ::

   urlpatterns = patterns('',
       (r'^jobvite/', include('jobvite.urls')),
       ...
   )

Additionally, you'll need to specify the URI to the Jobvite XML file: ::

    JOBVITE_URI = 'http://www.jobvite.com/CompanyJobs/Xml.aspx?c=XXXXX'

Use
---
Once installed and configured, you can query jobvite positions and obtain
results in JSON, keyed by jobvite ID. Any GET parameters will be used as
filter parameters. Example JSON: ::

    {
        'fxoOfv': {
            'title': 'Software Developer',
            'category': 'Engineering',
            'description': '...',
            'brief_description': '...',
            'job_type': 'Full-Time',
            'requisition_id': 1234,
            'apply_url': 'http://....',
            'detail_url': 'http://...',
            'location': 'Toronto, ON, Canada',
            'date': '4/21/2011'
        }
    }

jobvite aims at supporting various versions of django - including south and django migrations.

