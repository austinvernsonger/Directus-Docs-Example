Your Database
=====================

Choosing an Existing Schema
~~~~~~~~~~~~~~~~~~~~~~~~~~~

If you’re looking to get up and running as quickly or possible, you may
want to choose from our small but growing library of schema
boilerplates. Directus will also work with most SQL schemas you find
elsewhere – though the formatting of some table/field names may be less
intuitive to users.

Creating & Customizing Schemas
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Whether you’re adapting a preexisting database or starting from scratch
– the following guidelines will help you get the most out of Directus.
Below is an example SQL query for generating a simple table that
considers these guidelines:

.. code:: sql

    CREATE TABLE `articles` (
      `id` int(11) unsigned NOT NULL AUTO_INCREMENT,
      `active` tinyint(1) unsigned DEFAULT '2',
      `sort` int(11) DEFAULT NULL,
      `title` varchar(100) DEFAULT NULL,
      `article` text,
      `publish_date` datetime DEFAULT NULL,
      `author` int(11) DEFAULT NULL,
      PRIMARY KEY (`id`)
    ) ENGINE=InnoDB DEFAULT CHARSET=utf8;

Table & Field Naming
~~~~~~~~~~~~~~~~~~~~

Directus auto-formats all table and field names for presentation to the
users, so it’s important to consider your naming system. Beyond that –
you should make sure that your field names would make sense when
formatted and read by users.

-  Underscores become spaces
-  Each word is capitalized
-  Edge-cases are handled by an editable array of overrides
-  “\_id" is removed from the end of titles
-  Tables prepended with “directus\_” are hiden within Directus

*Great:* \* ``publish_date`` becomes “Publish Date” \*
``employee_number`` becomes “Employee Number” \* ``faq_and_support``
becomes “FAQ and Support”

*Not so great:* \* ``pubDate`` becomes “Pubdate” \* ``EmpNo`` becomes
“Empno” \* ``FaqSupport`` becomes “Faqsupport”

Primary Key
~~~~~~~~~~~

Currently Directus requires that every table contains an
auto-incremented primary key named ``id``.

.. code:: sql

    `id` int(11) unsigned NOT NULL AUTO_INCREMENT

    The abstracting/decoupling of this field name is under development.

Status Field
~~~~~~~~~~~~

If you would like the items of a table to track a “status” state, you
can easily do that within Directus. A status could be used in many
different ways, but the most common is: *Published*, *Draft*, or
*Deleted*, but you could extend or customize this as needed.

It is important when setting up an app to honor any Status states used
by Directus. Typically this means only showing active/published content.
Assuming you are using the default Status options, that would mean
limiting all SQL queries to:

.. code:: sql

    AND `active` = '1'

`Learn More`_

Sort Field
~~~~~~~~~~

Adding a ``sort(INT11)`` field to a table turns on Directus’
drag-and-drop sorting. Items on the Directus listing page will now have
handles for dragging them into curated orders. When sorted, Directus
will save ascending integers into the order field, thereby making it
easy to return results in this order:

.. code:: sql

    ORDER BY `sort` ASC

    If a table will likely have many items (), it may be advisable not
    to use the manual sort feature.

.. _Learn More: /04-developer/02-configuration.md