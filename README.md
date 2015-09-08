to do:
====================

- fix friendlyid redundancy issues on story-page slugs

- deploy a beta version of the new site on heroku

- make page count automated (e.g. page_count = Article.pages.count)

- manual slug overwrite option in article form

- on admin article view, [sort pages by page number](https://github.com/willisplummer/blog/blob/master/app/views/articles/admin.html.erb#L36)

- customize ckeditor to only provide basic functionality (bold, italic, link, indent, and linebreaks). it seems like this can be done using their toolbar configurator utility [found here](http://docs.ckeditor.com/#!/guide/dev_toolbar) but they suggest that you not just edit the config file because all of the plugins will still be pre-loaded. more info about the rails integration [here](https://github.com/galetahub/ckeditor).

- find a way of handling longer stories where the index on the first page is custom formatted w/ css

- update scrapers to skip leading `<br>`'s on page content and author bios. 

- improve layout to more accurately match the original. (figure out whether or not to keep the two leading linebreaks with page title.)

## done

- ~~scraper pulled all the `&nbsp`'s but the site doesn't like them. find and replace with `&nbsp;` before writing to db~~

- ~~validate author url input begins with http://~~

- ~~save password info in a private file~~

- ~~polymorphic pages that can be associated with articles or stories (which are nested under articles) - maybe STI would work for this purpose?~~

- ~~stories scraper for old site~~


setup:
====================
 ```
bundle
cp config/application.example.yml config/application.yml
 ```

(Enter the correct username and password for production in config/application.yml)
 
 ```
rake db:setup
rails s
 ```
