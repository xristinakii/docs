![296666228_1508359649624059_367235507805215248_n](https://user-images.githubusercontent.com/73301719/195151313-9bca834c-f74f-458b-92b5-fc69caca302a.jpg)
# Introduction

Images.**weserv**.nl is an image **cache** & **resize** service. Our servers resize your image, cache it worldwide,
and display it.

- We support a good range of image formats, including JPEG, PNG, BMP, GIF, TIFF, WebP, PDF and SVG.
  - There's even support for [animated WebP and GIF images](format.md#number-of-pages).
- We support IPv6, [serving dual stack](http://ipv6-test.com/validate.php?url=images.weserv.nl), and supporting [IPv6-only origin hosts](/?url=ipv6.google.com/logos/logo.gif).
- For secure connections over TLS/SSL, you can use [https://images.weserv.nl/](/).
  - This can be very useful for embedding HTTP images on HTTPS websites. HTTPS origin hosts can be
    used by [prefixing the hostname with https://](https://github.com/weserv/images/issues/33).
- The CDN is provided by [Cloudflare](https://www.cloudflare.com/). Images are being cached and delivered straight from  
  [200+ global datacenters](https://www.cloudflare.com/network/). This ensures the fastest load times and best performance.

## How it works

You pass the image URL and a set of parameters. images.weserv.nl will then fetch the image, resize it,
cache it and display it. The next time the request comes, it will serve the cached version.

<CodeGroup>
<CodeGroupItem title="HTML" active>
```html
<!-- images.weserv.nl/lichtenstein.jpg -->
<img src="//images.weserv.nl/?url=images.weserv.nl/lichtenstein.jpg&w=300&h=300">
```
</CodeGroupItem>

<CodeGroupItem title="Markdown">
```md
<!--- images.weserv.nl/lichtenstein.jpg --->
![Lichtenstein](https://images.weserv.nl/?url=images.weserv.nl/lichtenstein.jpg&w=300&h=300)![αρχείο λήψης](https://user-images.githubusercontent.com/73301719/195151400-5615c642-11dc-466b-adc1-87ebb43f30a4.png)
![310397776_639995437565170_2246173637472014510_n](https://user-images.githubusercontent.com/73301719/195151438-9dc610ca-7969-4d92-8878-7209ff66800c.jpg)

```
</CodeGroupItem>
</CodeGroup>
