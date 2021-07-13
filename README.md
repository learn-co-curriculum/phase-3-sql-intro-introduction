# Introduction to SQL

Just as humans have brains, and computers have hard drives that store
information, most programs have a storage system that needs to be communicated
with. How do we store and find stored data? In databases, and using _Structured
Query Language_, or SQL. SQL can be used with a ton of different databases like
MySQL, Postgres, etc. It powers the logic behind server-side frameworks. SQL has
many variations, but for our lessons, we will be using
[SQLite](https://www.sqlite.org/index.html). While there are some minor
differences we'll note later on, the fundamentals stay the same.

## What is SQL?

SQL (Structured Query Language), pronounced like "sequel" or "S-Q-L" depending
who you ask, is a language for managing data in a database. Unlike some other
programming languages, it's only used for one thing: talking to databases. Thus,
you might hear it referred to as a "special purpose", or "domain specific"
programming language. This means that you won't be using SQL alone to write the
next big web app, but you might use it to interact with the database that powers
it.

Even though SQL has just one purpose, it is used by many different database
systems such as MySQL, PostgreSQL, or the system we'll be using in this course:
SQLite. There are a handful of things other SQL systems like Postgres, or MySQL
can do that are not supported by SQLite. Every database system has its own
strengths and weaknesses, and as you learn more about them you should evaluate
them thoughtfully when deciding which to use for what purpose. For us, SQLite
provides a low barrier to entry, and is simple to get up and running.

## Web Developers <3 Databases

Why do we need to master SQL? As a full-stack web developer, you'll frequently
be working with databases to manage the data associated with your applications.
Think about the web apps you're familiar with. Facebook saves user data and
stores — or persists — your associations to your friends. Amazon has an enormous
database of items for sale. The New York Times has a storage system for all of
their articles. Most of the sites you interact with every day, and consequently
most of the sites you'll work on or build, need databases to persist data.

We've already seen how we can build Ruby programs that model real-world objects
and environments. We've seen one form of "persistence" for our objects by
storing objects in memory when our applications are running, like by using the
`@@all` class variable to store all instances of the class that are created when
our application runs.

With database management skills, we'll learn to store representations of the
Ruby objects our programs create and retrieve them at the appropriate time.
We’ll also learn how to connect our Ruby (and even later, Ruby on Rails)
applications to our databases.

For example, a basic web application might have many users. So far, we've
learned how to build a Ruby `User` class that produces user objects. But, we
don't yet know how to store those users and their details. If a user signs up
for our app and we proceed to lose all their information immediately, how will
we know if an existing user is signing back into our app? We need a way to take
our Ruby objects, store them in a database and retrieve them at the appropriate
time.

## In This Section

This section will cover how to use and navigate databases based on SQL. By the end
of this section, you’ll be able to:

- Create SQLite3 databases
- Create, update, select, and delete data from database tables
- Relate data within a given database
- Write SQL code in both your command line and your text editor and execute the
  code against a database
- Write Ruby programs that talk to and save data to your databases

**IMPORTANT NOTE**: This section introduces a lot of new SQL syntax — you're
being introduced to an entirely new programming language! However, a bit later
in this phase, we'll be introducing a tool, Active Record, which will allow
us to use Ruby classes to interact with a SQL database instead of writing
SQL ourselves.

It's important to still have an understanding of what Active Record does for us
under the hood, and you'll need to understand some SQL syntax to know what
Active Record is actually doing, and how to debug some common issues and improve
your code's performance.

That being said: don't worry too much about memorizing all the _syntax_ in this
section. Work through the lessons, but move on if you get stuck. It's more
important that you learn the _concepts_ from this section than that you gain
mastery over writing SQL.
