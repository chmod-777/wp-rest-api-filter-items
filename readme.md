# WP REST API Filter Items

A WordPress plugin that filter [WP REST API](http://wp-api.org/) items to your requirement.

## Description
The default for a post from the REST API fetch all data in `/wp-json/posts`. This plugin give you the chance to filter for the required fields. Add the items to  `GET` attribute on the url, like `wp-json/posts?items=ID,title,content` and you get only this fields.

#### Result for post, `wp-json/posts?items=ID,title,content`
```json
  {
    "ID": 1,
    "title": "Hello world!",
    "content": "<p>Welcome to <a href=\"http:\/\/localhost\/wpbeta\/\">WP Beta Dev Sites<\/a>. This is your first post. Edit or delete it, then start blogging!<br \/>\n:):)<\/p>\n<p> <\/p>\n<h3>Snippet #1<\/h3>Snippet #1 Content\n<div>\n<ul>\n<li>test<\/li>\n<\/ul>\n<\/div>\n<p><\/span><\/p>\n",
    "author": {...},
    "featured_image": null,
    "terms": {...}
  }
]
```

#### Result for taxonomy, `wp-json/posts?items=name,slug`.
```json
{
  "name": "Categories",
  "slug": "category",
  "labels": {...},
  "types": {...},
  "show_cloud": true,
  "hierarchical": true,
  "meta": {
    "links": {
      "archives": "http:\/\/localhost\/wpbeta\/plugins\/wp-json\/taxonomies\/category\/terms",
      "collection": "http:\/\/localhost\/wpbeta\/plugins\/wp-json\/taxonomies",
      "self": "http:\/\/localhost\/wpbeta\/plugins\/wp-json\/taxonomies\/category"
    }
  }
}
```

## Requirements
 * PHP 5.4
 * WordPress 4.*

## Kudos
Thanks a lot to D.Naber for his [Requiste Autoload](https://github.com/dnaber-de/Requisite).