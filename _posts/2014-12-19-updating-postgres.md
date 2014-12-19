---
layout: post
title:  "Quick Note on Updating Postgres.app"
date:   2014-12-19 16:30:00
categories: blog postgres rails
---

Yesterday, the Postgres dev team delivered a holiday gift - [Postgres 9.4](http://www.postgresql.org/about/news/1557/)! Since I like being an early adapter, I decided to upgrade to the latest version so I downloaded and installed the latest version of [Postgres.app](http://postgresapp.com/). Right after I updated, I fired up the Rails app I was working on this semester andddddd:

<img src="/img/pg-error.png" class="img-responsive" />

Wait, so what happened? I checked to make sure that Postgres.app was actually running and, since it was, I was scratching my head. Well, as it turns out, this was quite a simple fix.

When I installed the pg gem, I had to pass in the pg-config from Postgres.app which has the version number in it. Therefore, when I installed the new version of Postgres.app, it changed the path from `/Applications/Postgres.app/Contents/Versions/9.3/bin/pg_config` to `/Applications/Postgres.app/Contents/Versions/9.4/bin/pg_config`.

To solve this, go ahead and uninstall the pg gem (`gem uninstall pg`) and re-install it with the updated configuration (`gem install pg -- --with-pg-config=/Applications/Postgres.app/Contents/Versions/9.4/bin/pg_config`).

As a side note, all of your databases will be erased and you'll have to start anew. For those with Rails, you'll just have to run `rake db:create db:migrate` and you'll have your app up and running!
