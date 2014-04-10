# Installation


1. Clone this repo to your site-packages directory or anywhere on the path.

2. Add these settings to your sentry.conf.py file:

        AWS_ACCESS_KEY_ID = <Access Key>
        AWS_SECRET_ACCESS_KEY = <Secret Key>
        BACKUP_BUCKET_NAME = <The name of you S3 bucket>
        BACKUP_PATH = <Optional Root File Path>

3. Add this to the sentry.conf.py file to install into django:

        from sentry.conf import server
        server.INSTALLED_APPS += ('sentry_backup',)


Backups will run at 2AM by default. Change the periodic_task's crontab setting for a custom runtime.