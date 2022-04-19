# Actor - Dark Web Scraper

## Dark Web scraper

This actor allows you to scrape Dark Web sites. Within the OSINT support, you can use this actor to find sensitive information.

The Dark Web data scraper supports the following features:

-   Search any keyword - You can search any keyword you would like to have and get the results.

-   Scrape sensitive information - Scrape any sensitive information like emails, phones, API Keys or crypto wallets from Dark Web.

-   Scrape TOR - Since the actor supports TOR proxy, you can scrape any information up to your needs.

-   Customizable - If you are looking for a specific data, you can develop your own function and integrate into the scraper.

## Bugs, fixes, updates and changelog

This scraper is under active development. If you have any feature requests you can create an issue from [here](https://github.com/tugkan/darkweb-scraper/issues).

## Input Parameters

The input of this scraper should be JSON containing the list of pages on Dark Web that should be visited. Required fields are:

| Field                | Type    | Description                                                                                                                                                                                                    |
| -------------------- | ------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| search               | String  | (optional) Keyword that you want to search on Dark Web.                                                                                                                                                       |
| startUrls            | Array   | (optional) List of Dark Web URLs.                                                                                                                  |
| maxDepth              | Integer | (optional) Maximum depth the scraper will dive into. If you want to scrape a Dark Web site in a very superficial way, you can set this with a low number.                                                          |
| maxPages             | Integer | (optional) You can limit scraped pages. This should be useful when you search through the big websites.                                                                                                |
| extendOutputFunction | String  | (optional) Function that takes a JQuery handle ($) as argument and returns object with data                                                                                                                    |

##### Tip

When you want to have a scrape over a specific URL, just copy and paste the link as one of the **startUrl**.

If you would like to scrape the website quickly without diving into its deeper pages, you can set `maxDepth` option within a lower number.


### Compute Unit Consumption

The actor optimized to run blazing fast and scrape many as pages as possible. If actor doesn't block very often it'll scrape 100 pages in 5 seconds with ~0.1-0.2 compute units.

### Dark Web Scraper Input example

```json
{
  "startUrls":[
    "http://xjfbpuj56rdazx4iolylxplbvyft2onuerjeimlcqwaihp3s6r4xebqd.onion/"
  ],
  "search": "Dark Web",
  "maxDepth": 5,
  "maxPages": 10,
}
```

## During the Run

During the run, the actor will output messages letting you know what is going on. Each message always contains a short label specifying which page from the provided list is currently specified.
When items are loaded from the page, you should see a message about this event with a loaded item count and total item count for each page.

If you provide incorrect input to the actor, it will immediately stop with failure state and output an explanation of what is wrong.

## Dark Web Export

During the run, the actor stores results into a dataset. Each item is a separate item in the dataset.

You can manage the results in any languague (Python, PHP, Node JS/NPM). See the FAQ or <a href="https://www.apify.com/docs/api" target="blank">our API reference</a> to learn more about getting results from this Dark Web actor.

## Scraped Properties

The structure of each item in Dark Web Scaper looks like this:

### Item Detail

```json
{
  "url": "http://xjfbpuj56rdazx4iolylxplbvyft2onuerjeimlcqwaihp3s6r4xebqd.onion/cellar-door/",
  "links": [
    "http://ogp.me/ns",
    "http://ogp.me/ns/fb",
    "http://xjfbpuj56rdazx4iolylxplbvyft2onuerjeimlcqwaihp3s6r4xebqd.onion/cellar-door/",
    "https://schema.org/WebPage",
    "https://schema.org/SiteNavigationElement",
    "http://xjfbpuj56rdazx4iolylxplbvyft2onuerjeimlcqwaihp3s6r4xebqd.onion/",
    "http://xjfbpuj56rdazx4iolylxplbvyft2onuerjeimlcqwaihp3s6r4xebqd.onion/faq/",
    "http://xjfbpuj56rdazx4iolylxplbvyft2onuerjeimlcqwaihp3s6r4xebqd.onion/support/",
    "http://xjfbpuj56rdazx4iolylxplbvyft2onuerjeimlcqwaihp3s6r4xebqd.onion/privacy-notice/",
    "http://xjfbpuj56rdazx4iolylxplbvyft2onuerjeimlcqwaihp3s6r4xebqd.onion/sitemap/",
    "http://xjfbpuj56rdazx4iolylxplbvyft2onuerjeimlcqwaihp3s6r4xebqd.onion/stream-recording/",
    "http://xjfbpuj56rdazx4iolylxplbvyft2onuerjeimlcqwaihp3s6r4xebqd.onion/art/",
    "http://xjfbpuj56rdazx4iolylxplbvyft2onuerjeimlcqwaihp3s6r4xebqd.onion/color-artwork/",
    "http://xjfbpuj56rdazx4iolylxplbvyft2onuerjeimlcqwaihp3s6r4xebqd.onion/music/",
    "http://xjfbpuj56rdazx4iolylxplbvyft2onuerjeimlcqwaihp3s6r4xebqd.onion/sketch-books/",
    "http://xjfbpuj56rdazx4iolylxplbvyft2onuerjeimlcqwaihp3s6r4xebqd.onion/category/txt/stories/",
    "http://xjfbpuj56rdazx4iolylxplbvyft2onuerjeimlcqwaihp3s6r4xebqd.onion/text/",
    "http://xjfbpuj56rdazx4iolylxplbvyft2onuerjeimlcqwaihp3s6r4xebqd.onion/category/txt/blog/",
    "http://xjfbpuj56rdazx4iolylxplbvyft2onuerjeimlcqwaihp3s6r4xebqd.onion/category/txt/guides/",
    "http://xjfbpuj56rdazx4iolylxplbvyft2onuerjeimlcqwaihp3s6r4xebqd.onion/category/txt/metaverse/",
    "http://xjfbpuj56rdazx4iolylxplbvyft2onuerjeimlcqwaihp3s6r4xebqd.onion/category/txt/rant/",
    "http://xjfbpuj56rdazx4iolylxplbvyft2onuerjeimlcqwaihp3s6r4xebqd.onion/download/",
    "http://xjfbpuj56rdazx4iolylxplbvyft2onuerjeimlcqwaihp3s6r4xebqd.onion/audio-testing/",
    "http://xjfbpuj56rdazx4iolylxplbvyft2onuerjeimlcqwaihp3s6r4xebqd.onion/contact/",
    "https://schema.org/CreativeWork",
    "http://www.anubianhost.com/account/aff.php",
    "https://floatoverblow.com",
    "http://furrystuff.com/",
    "http://www.infochammel.com/",
    "http://www.jillianmayer.net/",
    "http://www.kainless.com/",
    "http://www.kainless.com",
    "https://www.jwz.org/",
    "https://lameazoid.com/",
    "https://emreed.net/LowTech_Directory.html",
    "https://wiby.me/",
    "https://web.archive.org/web/20080915204851/http",
    "https://www.nevermindstu.com",
    "https://www.youtube.com/channel/UC-CEC8G9v3ry2VOllsJNVYw",
    "https://www.twitch.tv/funkyjoe86",
    "https://www.numou.net/",
    "https://aronsmusings.wordpress.com/",
    "https://physonyl.net",
    "https://protohub.online/",
    "https://blog.protohub.online/JourneyOfTheProtogen/",
    "http://www.rantradio.com/",
    "http://www.rant.social/",
    "https://repair.org",
    "http://www.thisismymilwaukee.com",
    "https://www.youtube.com/watch",
    "http://xjfbpuj56rdazx4iolylxplbvyft2onuerjeimlcqwaihp3s6r4xebqd.onion/tor-networks/",
    "http://phobosxilamwcg75xt22id7aywkzol6q6rfl2flipcqoc4e4ahima5id.onion/",
    "http://underdiriled6lvdfgiw4e5urfofuslnz7ewictzf76h4qb73fxbsxad.onion/",
    "http://wclekwrf2aclunlmuikf2bopusjfv66jlhwtgbiycy5nw524r6ngioid.onion",
    "http://meynethaffeecapsvfphrcnfrx44w2nskgls2juwitibvqctk2plvhqd.onion",
    "http://galaxy3bhpzxecbywoa2j4tg43muepnhfalars4cce3fcx46qlc6t3id.onion",
    "http://tor66sewebgixwhcqfnp5inzp5x5uohhdy3kvtnyfxc2e5mxiuh34iid.onion",
    "http://y5wnzw4e6i7srm2gqadlow5anhlaj5avdkzbwzbmrxwkygxdp7ffieqd.onion/",
    "http://absjpxsvyn5cboihzenbyfngq224rpvtfgnehwwvkhjm3gmk6oruhoad.onion/blog/",
    "http://qrtitjevs5nxq6jvrnrjyz5dasi3nbzx24mzmfxnuk2dnzhpphcmgoyd.onion/",
    "http://xjfbpuj56rdazx4iolylxplbvyft2onuerjeimlcqwaihp3s6r4xebqd.onion/lbry-and-odysee-a-video-hosting-review/",
    "http://xjfbpuj56rdazx4iolylxplbvyft2onuerjeimlcqwaihp3s6r4xebqd.onion/web-3-0/",
    "http://xjfbpuj56rdazx4iolylxplbvyft2onuerjeimlcqwaihp3s6r4xebqd.onion/clarification-time/",
    "http://xjfbpuj56rdazx4iolylxplbvyft2onuerjeimlcqwaihp3s6r4xebqd.onion/nginx-image-format-wars/",
    "http://xjfbpuj56rdazx4iolylxplbvyft2onuerjeimlcqwaihp3s6r4xebqd.onion/presearch/",
    "http://xjfbpuj56rdazx4iolylxplbvyft2onuerjeimlcqwaihp3s6r4xebqd.onion/site-supported-codec-guidelines/",
    "http://xjfbpuj56rdazx4iolylxplbvyft2onuerjeimlcqwaihp3s6r4xebqd.onion/web-3-0/comment-page-1/",
    "http://www.musex.space",
    "http://xjfbpuj56rdazx4iolylxplbvyft2onuerjeimlcqwaihp3s6r4xebqd.onion/rollerblade-office-caster-wheels-buyer-beware/comment-page-4/",
    "http://xjfbpuj56rdazx4iolylxplbvyft2onuerjeimlcqwaihp3s6r4xebqd.onion/chinese-xbox-360-wireless-receiver-driver-setup/comment-page-35/",
    "http://wolfballs.com",
    "http://xjfbpuj56rdazx4iolylxplbvyft2onuerjeimlcqwaihp3s6r4xebqd.onion/xbox-dvd-remote-everything/comment-page-1/",
    "https://schema.org/WPFooter",
    "https://www.s-config.com",
    "http://xjfbpuj56rdazx4iolylxplbvyft2onuerjeimlcqwaihp3s6r4xebqd.onion"
  ],
  "emails": [],
  "phones": [],
  "cryptoAddresses": {},
  "misc": {
    "Twitter username": [
      "@S_Config"
    ],
    "Instagram username": [
      "@S_Config"
    ]
  },
  "searchKeywordFound": false
}
```
