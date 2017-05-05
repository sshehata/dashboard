# Contexta

> Latest snapshot of production code

Every time new frontend code is deployed the production code is pushed here on [github](https://github.com/kuus/contexta) and the source code on the private repo on [gitlab](https://gitlab.com/kuus/contexta)

## Deploy

Simply copy all the files from this repo in your server folder.

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

Open the terminal in the folder with the files of this repo and run a simple local server, e.g. [with python](http://www.linuxjournal.com/content/tech-tip-really-simple-http-server-python):
```bash
$ cd /home/contexta/app
$ python -m SimpleHTTPServer
```
Open the browser at http://127.0.0.1:8000

