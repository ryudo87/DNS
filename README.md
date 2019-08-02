## Domain name system

<p align="center">
  <img src="http://i.imgur.com/IOyLj4i.jpg"/>
  <br/>
  <i><a href=http://www.slideshare.net/srikrupa5/dns-security-presentation-issa>Source: DNS security presentation</a></i>
</p>

A Domain Name System (DNS) translates a domain name such as www.example.com to an IP address.

Your router or **ISP** provides information about which DNS server(s) to contact when doing a lookup.  
Lower level DNS servers cache mappings, which could become stale due to DNS propagation delays.  
DNS results can also be cached by your browser or OS for a certain period of time, determined by the **[time to live (TTL)]**


### Disadvantage(s): DNS

* a slight delay, although mitigated by caching described above.
* [DDoS attack](http://dyn.com/blog/dyn-analysis-summary-of-friday-october-21-attack/), preventing users from accessing websites 



## Content delivery network


### Push CDNs

Push CDNs receive new content whenever changes occur on your server.  
providing content, uploading directly to the CDN and rewriting URLs to point to the CDN.  


Sites with a small amount of traffic or sites with content that isn't often updated work well with push CDNs.  Content is placed on the CDNs once, instead of being re-pulled at regular intervals.

### Pull CDNs

Pull CDNs grab new content from your server  **when the first user requests the content**.  
You leave the content on your server and rewrite URLs to point to the CDN. 

A [time-to-live (TTL)]

### Disadvantage(s): CDN

* CDN costs could be significant 
* Content might be stale if it is updated before the TTL expires it.
* CDNs require **changing URLs for static content to point to the CDN**.
