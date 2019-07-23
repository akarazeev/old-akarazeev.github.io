---
title: PostgreSQL Database with specific locale
lang: en
ref: postgresql220719
date: 2019-07-22 03:00:01 +03:00
tags:
- PostgreSQL
- SQL
- Mac OS
layout: post
header:
  teaser: "/images/postgresql.jpg"
---

Creating database with specific locale:
```
CREATE DATABASE <db_name>
    LC_COLLATE 'ru_RU.UTF-8' LC_CTYPE 'ru_RU.UTF-8'
    TEMPLATE template0;
```
