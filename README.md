# AcyOrt

A Node.js blog tool powered by GitHub.

You can write you blog on `GitHub issue` and publish it on `Your Own Domain` use `GitHub page`

### Demo

http://acyort.am0200.com/

Site content from here: https://github.com/LoeiFy/AcyOrt/issues

### Usage

#### # Add Blog Posts

1 . Add Posts

Select your `Repo` one and add content on `issue` 

Example: https://github.com/LoeiFy/AcyOrt/issues

2 . Add Page

Set the issue `title` after `[page name]`

Example: https://github.com/LoeiFy/AcyOrt/issues/3

3 . Add post summary

Just add `<!-- more -->` tag after summary

Example: https://github.com/LoeiFy/AcyOrt/issues/2

4 . Add tags

Just add issue `Labels`

#### # Build Your Blog

0 . Fork and Switch to branch `gh-pages`

1 . Delete files(Optional)

```
./archives
./page
./pages
./posts
./tags
./index.html
./rss.xml
```

2 . Install modules
  
```bash
$ npm i
```

3 . Modify `config.js`

```js
// config
module.exports = {
    url:        'http://acyort.am0200.com',                     // Site Url
    title:      'AcyOrt',                                       // Blog Title
    about:      'A Node.js blog tool powered by GitHub.',       // Blog Info    
    user:       'LoeiFy',                                       // Your GitHub UserName
    repo:       'AcyOrt',                                       // Your GitHub issue Repo    
    rss:        '/rss.xml',                                     // RSS Link
    perpage:    5,                                              // Posts Per Page
    token:      ''+'',                                          // GitHub Access Token(Optional)
    authors:    [],                                             // Post Authors(filter author)
    duoshuo:    '',                                             // Duoshuo shortname
    disqus:     '',                                             // Disqus shortname
    menu: [                                                     // Menu
        {name: 'home', url: '/'},
        {name: 'about', url: '/page/about/'},
        {name: 'archives', url: '/archives/'}
    ]
}
```

4 . Modify `CNAME`, add your domain

5 . Build website

```bash
$ npm run build
```

5.5 . you can run local test: `http://127.0.0.1:2222`

```bash
$ npm run start
```

6 . `git add` and `git push` to publish your posts

### Feature

- [x] Post 

	`./posts/yyyy/mm/...`
  
- [x] Comment 

	`Disqus` or `Duoshuo`

- [x] Archives

	`./archives/`
  
- [x] Rss
 
 	`./rss.xml`
  
- [x] Page 

	`./page/.../`

- [x] Tags 

 	`./tags/.../`

- [x] Menu

- [ ] prev post & next post

### License

MIT