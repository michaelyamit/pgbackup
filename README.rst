pgbackup
========

CLI for backup remote PostgreSQL database either locally or to S3.

Preparing the Development
-------------------------

Ensure ``pip`` and ``pipenv`` are installed.
Clone repository: ``git clone git@github.com:michaelyamit/pgbackup``
``cd`` into the repository.
Fetch development dependencies ``make install``
Activate virtualenv: ``pipenv shell``

Usage
-----

Pass in a full database URL, the storage driver, and the destination.

S3 Example w/ bucket name:

::

	$ pgbackup postgres://bob@example.com:5432/db_one --driver s3 backups

Local Example w/ local path:

::

	$ pgbackup postgres://bob@example.com:5432/db_one --driver local /var/local/db_one/bakcups/dump.sql

Running Tests
-------------

Run tests locally using ``make`` if virtualenv is active:

::

	$ make

If virtualenv isn't active then use:

::

	$ pipenv run make
