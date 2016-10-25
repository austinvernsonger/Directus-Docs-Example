What is Directus
=====================


Directus is a free and open-source headless CMS for intuitively managing custom-schema database content.


----------

A Familiar Problem
++++++++++++++++++++

As a developer, you're probably already managing database content directly through Sequel-Pro, phpMyAdmin, or the command line. These are excellent tools because you get complete control with little setup beyond entering the database credentials. But you would never give that access to clients, designers, or even inexperienced engineers – relationships, validation, media, and security can easily get unwieldy. Not to mention you'll either have to build within one of those all-encompassing proprietary CMS designed for blogs, or build a _custom_ CMS from the ground-up.


Custom Databases, No Workflow Assumptions
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

Directus allows developers to build projects with custom, scalable, and decoupled databases. No more proprietary templating systems and plugin piecemealing. Build with whichever technologies are most appropriate and then either connect  directly to the database, via the Directus API, or use one of our SDKs. This makes it perfect for native-apps, web-apps, physical installations, and even projects that span multiple platforms.

Headless CMS
++++++++++++++++++++

Once you have a basic database you'll likely want to start creating, editing, and managing its content. Directus gives even the most novice users the ability to safely and intuitively manage database content directly. Since it pulls all of its architecture and configuration directly from the schema, there's no need for time-consuming setup.

Comparison of data/content management options
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

+----------------------------------------------+-------------+-----------------+----------------------------------+
| Feature                                      | Directus    | DB Client       | Typical CMS                      |       
+==============================================+=============+=================+==================================+
| Manages existing (custom-schema) databases   |             |                 |                                  |
+----------------------------------------------+-------------+-----------------+----------------------------------+
|Works for non-website projects                |             |                 |                                  |
+----------------------------------------------+-------------+-----------------+----------------------------------+
|Allows custom SQL queries                     |             |                 |                                  |
+----------------------------------------------+-------------+-----------------+----------------------------------+
|Granular table/field user permissions         |             |                 |                                  |
+----------------------------------------------+-------------+-----------------+----------------------------------+
|Intuitive for non-developers                  |             |                 |                                  |
+----------------------------------------------+-------------+-----------------+----------------------------------+
|Interface for relational data                 |             |                 |                                  |
+----------------------------------------------+-------------+-----------------+----------------------------------+
|Interface for files/media                     |             |                 |                                  |
+----------------------------------------------+-------------+-----------------+----------------------------------+
|Data API                                      |             |                 |                                  |
+----------------------------------------------+-------------+-----------------+----------------------------------+
|Free and open-source                          |             |                 |                                  |
+----------------------------------------------+-------------+-----------------+----------------------------------+



----------

What about my website, app, or project?
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

Directus only manages the content in your database, beyond that you can use whatever technologies best fit your project. Not accustomed to so much freedom? Here are three easy ways to connect/access your data:

* **API**: Use the Directus API to add/update/delete records or fetch JSON data
* **Directus Library**: Use the directus library of functions to interact with the database
* **SQL Queries**: Ignore Directus altogether, connect directly to the database, and use custom SQL queries

----------

Or don't connect anything at all!
+++++++++++++++++++++++++++++++++++

With the ability to create and manage any database schema you can dream up, maybe Directus **is** the project. Instead of paying $20/month for a rigid Project Management service, just throw together a quick schema with fields customized to your needs. Now you have a free solution that can easily be extended to accommodate any new info you want to track.


Example Schema: Project Management
+++++++++++++++++++++++++++++++++++

.. literalinclude:: Example_Schema.txt
    :language: txt
    :lines: 1-36

