---
layout: post
title: Tips - Importing data into sqlite3 database from another sqlite3 database.
categories: tips
---

SQLite3 provides [ATTACH DATABASE](http://www.sqlite.org/lang_attach.html) statement to add another database file to current database connection.

Use this statement to connect to source database:
{% highlight sql %}
> ATTACH DATABASE source_db AS source_db;
{% endhighlight %}

Then use INSERT...SELECT to import data from source database to destination tabel(e.g. cities table):

{% highlight sql %}
> INSERT INTO cities(name) SELECT name FROM source_db.cities;
{% endhighlight %}

