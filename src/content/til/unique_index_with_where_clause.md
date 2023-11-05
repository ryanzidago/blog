---
title: "Unique index with where clause"
description: "Unique index with where clause"
pubDate: '2023-11-04'
tags: ["database"]
---

Let's say that you have a `customers` table. 
Each `customer` can have many `templates`, but only one of those `templates` should be `default`. 
You can create a unique index with a `WHERE` clause like so in SQL/PostreSQL:

```sql
CREATE UNIQUE INDEX unique_default_template_per_customer_index ON templates (customer_id)
WHERE is_default = true;
```

Live example <a href="https://www.db-fiddle.com/f/qPKWddsW8vTmpn6eFvjYRG/0" target="_blank">here</a>.