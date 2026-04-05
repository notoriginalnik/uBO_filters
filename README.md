# uBO_filters

<a href="abp:subscribe?location=https://raw.githubusercontent.com/notoriginalnik/uBO_filters/refs/heads/main/duckduckgo.txt&title=uBO_filters">subscribe on html.duckduckgo_filter</a>  
[subscribe on html.duckduckgo_filter](abp:subscribe?location=https://raw.githubusercontent.com/notoriginalnik/uBO_filters/refs/heads/main/duckduckgo.txt&title=uBO_filters)  
https://github.com/notoriginalnik/uBO_filters/raw/refs/heads/main/stackoverflow.txt  
https://github.com/notoriginalnik/uBO_filters/raw/refs/heads/main/github.txt  
https://github.com/notoriginalnik/uBO_filters/raw/refs/heads/main/wikipedia.txt  

Для поиска чаще использую `html.duckduckgo.com`, с одним синтаксисом пока не определился: 
```
html.duckduckgo.*##.results > div:has(a[href*="/reddit.com"])
html.duckduckgo.*##a[href*="/soundcloud.com/"]:upward(div):remove()
html.duckduckgo.*##.results > div:has(a:is(a[href*="www.amazon."], a[href*="/amazon.de"], a[href*="/amazon.com"], a[href*="/amazon.nl"], a[href*="/amazon.ca"]))

```

Примеры для других поисковиков:
```
duckduckgo.com,bing.com,ya.ru##a[href*="forkful.ai"]:upward(li):remove()
google.com##a[href*="forkful.ai"]:upward(2):remove()

```

## Прочее

Помимо `https://html.duckduckgo.com/html/` есть еще `https://lite.duckduckgo.com/lite/`, 
но его неудобно фильтровать.


С одной стороны сущности можно не множить, когда блокировщик уже есть.
Но специально для фильтрации поиска есть удобное расширение https://github.com/iorate/ublacklist.


Разные фильтры можно найти на сайте https://filterlists.com/


В [манифесте](https://github.com/gorhill/uBlock/blob/master/platform/firefox/manifest.json) 
указаны наиболее популярные сайты где выкладывают фильтры, и где работают ссылки подписки вида
`abp:subscribe?location=`:
```
        "https://easylist.to/*",
        "https://*.fanboy.co.nz/*",
        "https://filterlists.com/*",
        "https://forums.lanik.us/*",
        "https://github.com/*",
        "https://*.github.io/*"
```