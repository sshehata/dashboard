# Contexta

> Latest snapshot of production code

Every time new frontend code is deployed the production code is pushed here on [github](https://github.com/kuus/contexta) and the source code on the private repo on [gitlab](https://gitlab.com/kuus/contexta)

The website is always accessible from [contexta.kunderikuus.net](http://contexta.kunderikuus.net) (*http*) and [kuus.github.io/contexta](https://kuus.github.io/contexta) (*https*)

## Deploy

Delete the html tag `<base href="/contexta/">` from the file `index.html` and then copy all the files from this repository in your server folder.

### Switch backend urls
Before to deploy open the file `index.html` and edit the `<script>` tag that you see [in these lines](https://github.com/kuus/contexta/blob/gh-pages/index.html#L2-L4) with the urls you need:
```html
<script>window.URLS = {
  overstappen: 'https://www.contextaservices.com:8443/',
  nuon: 'https://contextaservices.com:10443/',
  reuters: 'http://contextaservices.com:9080/'
};</script>
```
Note that you don't have to define all these the backend URLs but just those whose default value you want to override. The urls in the above snippet of code are the default values (as you can see [in this file](https://gitlab.com/kuus/contexta/blob/master/src/app/common/api/service.js#L13-17))

### Run locally

Delete the html tag `<base href="/contexta/">` from the file `index.html` and then open the terminal in the folder with the files of this repo and run a simple local server, e.g. [with python](http://www.linuxjournal.com/content/tech-tip-really-simple-http-server-python):
```bash
$ cd /home/contexta/app
$ python -m SimpleHTTPServer
```
Open the browser at http://127.0.0.1:8000


## Source

### Starter

Project bootstrapped with [NG6-starter](https://github.com/AngularClass/NG6-starter)

Create a new component with:
```
gulp component -- --name footer --parent ../common
```

### Libraries:

- [angular-material](https://github.com/angular/material)
- [angular-data-grid](https://github.com/angular-data-grid/angular-data-grid.github.io)
- [angular-material-data-table](https://github.com/daniel-nagy/md-data-table) (only css)
- [xml2js](https://www.npmjs.com/package/xml2js)
- [zenscroll](https://github.com/zengabor/zenscroll)
- ...see package.json


### To keep an eye on

- angular material datepicker issues: http://stackoverflow.com/questions/41324991/angular-material-datepicker-opening-position-is-wrong-in-chrome and [github issue](https://github.com/angular/material/issues/10144) and [this issue too](https://github.com/angular/material/issues/10209)
