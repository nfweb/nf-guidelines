This document describes the proposed URL schemata for Nightfever Web Services.

#Domain Names

The main domain is ```nightfever.org```.

```www```-subdomains are considered deprecated and should be redirected to the corresponding www-free (sub)domain. ```www.nightfever.org``` -> ```nightfever.org```, ```www.koeln.nightfever.org``` -> ```koeln.nightfever.org```

##Internationalized Domain Name (IDN)
Subdomains should not contain non-latin characters, since IDNs are still facing some implementation problems.

However there may be redirects to the transilerated subdomain (```köln.nightever.org``` = ```xn--kln-sna.nightfever.org``` ->  ```koeln.nightfever.org```).

## Other Domain Names
Due to historic reasons, most nightfever sites have their own domain name ```nightfever-:city.de```. The main site uses ```nightfever-online.de```.
These legacy domains should be redirected to the new domains for nightfever.org

Additionally there are some nightfever websites with different domain schemes (and using their own CMS).

* [nightfeverchicago.org](http://nightfeverchicago.org/)
* [nightfeverbxl.be](http://nightfeverbxl.be/)
* [nightfeverliege.be](http://nightfeverliege.be/)
* [nightfever-weekend.com](http://nightfever-weekend.com/)

**All existing domain names should stay in place but redirect to the new main domain.**

##URL Shortener
* shortens urls for easy sharing (micorblogging, f2f meet)
* CMS integration assists brand recognition (in contrast to a generic shortener like bit.ly

**Suggestions:** ```n8fvr.it```, ```n8fever.org```, ```nght.fr``` or the like

#Sites & Subdomains
Sites for specific nightfever projects reside in their own subdomains. 

Projects include teams, events and services on local, regional and global scale.

Conflicting subdomains should have a clear precedence. 

##Local Cities
Subdomains for local nightfever cities are derived from their name or an appropriate abbreviation. 
Examples: ```koeln.nightfever.org```, ```fulda.nightfever.org```, ```valencia.nightfever.org```, ```new-york.nightfever.org```

##Events and projects
Subdomains for specific events and project are derived from their name or an appropriate abbreviation.
If a recurring event requires speficic sites for each recurrance, the subdomain is constructed from core identifiable features such as year, place or name.  

Examples: ```weekend.nightfever.org```, ```fulda14.nightfever.org```, ```academy.nightfever.org```,  ```nfweb.nightfever.org```

##Services
Subdomains for specific services are derived from their name or an appropriate abbreviation.
Examples: ```mail.nightfever.org```, ```auth.nightfever.org```, ```cdn.nightfever.org```, ```shop.nightfever.org```

##Regions
Pages for specific regions (e.g. countries) should not get their own subdomains but live in the main scope.

Region identifiers are derived from their country code as defined by ISO 3166-1 [List on Wikipedia](http://en.wikipedia.org/wiki/ISO_3166-1)

#Query Paths
The first component of a path defines the language, in which the requested page is to be dispayed.

The language identifier may be omitted if the default language of a site is by far the most important one (this includes single-language pages).

The other components of a path specify the requested page and its content.

Paths should be clean, user-friendly and seo-friendly.

##Static Content
The path of static pages consists of human-readable words in the language of the specified page. Subdirectories may be used when necessary.

##Dynamic Content
Paths for dynamic content should include the type of content, the content id and a human readable title. Other properties may be included if they provide major information (e.g. event dates).

**TODO:** further specification of url components. allowed characters. transliteration. schemata for specific content types.

Example: ```/news/123456/a-new-nightfever-website-has-launched```, ```/events/123457/2014-03-14-international-nightfever-weekend-in-fulda```

##Landing Page Redirects
Every site on its own subdomain may also be accessed via redirect from the correspondent path on the main domain.
Example: ```nightfever.org/mail``` -> ```mail.nightfever.org```, ```nightfever.org/köln``` -> ```koeln.nightfever.org```, ```nightfever.org/koeln``` -> ```koeln.nightfever.org```

##Short URLS
Short urls consist of only the content id (and possibly an identifier for short-urls) and redirect to the full path.

Example: ```/go/123456``` -> ```/news/123456/a-new-nightfever-website-has-launched```

#Error Pages
* non-existing subdomains
* non-existing paths
* non-existing languages