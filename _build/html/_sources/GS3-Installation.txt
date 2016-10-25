Installation
=====================

Server Preparation
~~~~~~~~~~~~~~~~~~

1. Check that your server meets the `requirements`_
2. Download and unzip the Directus package from `here`_
3. Create a database and MySQL user with access/modify privileges on
   your server

-  You can also use an existing database, but it’s worth taking a look
   at the typical `Directus Schema`_

4. Upload the files to a public directory on your server
5. Run the installation script by accessing the URL where you uploaded
   the files

--------------

Installation Walkthrogh
~~~~~~~~~~~~~~~~~~~~~~~

Step 0 – Requirements
^^^^^^^^^^^^^^^^^^^^^

This pre-installation step will only be shown if the server requirements
are not met.

Step 1 – Project Info
^^^^^^^^^^^^^^^^^^^^^

-  *Project Name* – The name of this project
-  *Project Path* – This should auto-fill, but it’s the path of this
   install
-  *Admin Email* – The email address for your first Directus user/admin
-  *Admin Password / Confirm* – The password for your first Directus
   user/admin

Step 2 – Database
^^^^^^^^^^^^^^^^^

-  *Database Type* – The database type to be used. (Only MySQL is
   supported, including MariaDB, Percona Server or equivalent). *SQLite
   and PostgreSQL support are under development at the moment*
-  *Host Name* – The database host, typically ``localhost``
-  *Host Port* - The database host port
-  *Username* – The database user with access and modify privileges
-  *Password* – The password for that database user
-  *Database Name* – The name of an existing database to be managed
-  *Install Schema* – List of optional boilerplate schemas

Step 3 – Confirmation
^^^^^^^^^^^^^^^^^^^^^

-  If the database connection succeeds you’ll be shown an installation
   summary page and given an opportunity to email these details to the
   admin user.

    **Security Note:** Once you have completed the install, make sure to
    delete install folder.

--------------

Troubleshooting
~~~~~~~~~~~~~~~

If you’re having problems with your Directus install, please visit our
`troubleshooting section`_.

-  `Server error occurred!`_
-  `Enable mod\_rewrite`_

.. _requirements: /01-getting-started/02-requirements.md
.. _here: https://github.com/directus/directus/tree/build
.. _Directus Schema: /04-developer/06-schema-guide.md
.. _troubleshooting section: /05-troubleshooting
.. _Server error occurred!: #
.. _Enable mod\_rewrite: /05-troubleshooting