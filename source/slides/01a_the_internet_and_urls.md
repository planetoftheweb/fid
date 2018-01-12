<!-- .slide: data-state="title" -->
# The Internet and URLs

---

# How the internet works

- Client makes a request to a server.
- The server routes the request to a service
- Server sends data back to client

> > Teacher's Notes:

Before we get started, let's talk a bit about how the internet works. You probably already know generally speaking how it works, but I think it would help to cover more specifically what it's doing in the background

First There's two types of computers on the internet...clients and servers. Any computer can behave as a client or a server. A client is the computer that makes requests for information to a server.

The server has special software installed that sends the request for the information to a service. That's usually some application that does something with the requests. You could be requesting a webpage, or an email. The server will analyze the request and then send it to the appropriate application to process.

Finally, once the server finishes requesting the information, it's sent back to the client as a webpage, an email, or whatever.

---

## Internet Protocols

- Communication happens through protocols
- Various server apps handle different [protocols](http://en.wikipedia.org/wiki/Internet_Protocol)
- http, pop, smtp, ftp, https

> > Author's Notes

On the internet, communication happens through protocols. If you've seen Star Wars you might remember that C3-PO is a protocol droid and that he got hired by Luke's uncle because he spoke the language of moisture vaporators.

The internet is a bit like that, in order to get things done, you have to be able to communicate in different languages. Each service has it's own language or 'protocol'. When requests are made to the server, they happen in these different languages.

By far, the most common protocol is http. You usually see it typed at the beginning of a web address, but there are others like pop and smtp for mail, ftp for file transfers and https for secure web connections.

---

## Uniform Resource Locator

<small>[https://www.youtube.com/watch?v=MspVCc0_R3g&t=37s#top](https://www.youtube.com/watch?v=MspVCc0_R3g&t=37s#top)</small>

- The initial request/command

> > Author's Notes:

You might be asking how the server knows what to do. The key to that magic is the URL or Uniform Resource Locator. You're probably used to seeing the on the web. They have all the information the server needs to do it's job.

This is a pretty complex looking URL, but it's divided into several different parts and it's important that you understand how these work.

Note: Sometimes the server will have a shortened version of this without all of the information to make it easier to read.

---

## Protocol
<small>**https:**//www.youtube.com/watch?v=MspVCc0_R3g&t=37s#top</small>


- Language of the request
- http vs https

> > Author's Notes

The first piece of the request is the protocol. This is the main thing the server needs to know, so that it can send the request to the proper service or application. Here, it's https, because it's an http request that's a bit more secure.

Most modern sites today use https instead of http because it's a more secure version in which pages are sent encrypted.

---

## Subdomain

<small>https:// **www** .youtube.com/watch?v=MspVCc0_R3g&t=37s#top</small>


- Domain inside domain
- Helps you divide requests

> > Author's Notes

Servers have a lot of ways to divide requests and one of the ways you can do that is by using a sub-domain. A sub-domain allows the same domain to do multiple jobs. It's like having a website inside another website.

You've probably noticed that most websites have a www. subdomain, but there can be others, so for example, you can go www.google.com for web searches, images.google.com to do image specific searches or mail.google.com to use your google email.

---

## Domain

<small>https://www. **youtube ** .com/watch?v=MspVCc0_R3g&t=37s#top</small>

- The location of a service [on the internet](https://www.google.com/search?q=ip+address)
- Converted to IP addresses by DNS Servers
- IP addresses = Zip Codes
- DNS Servers = Post Office

> > Author's Notes

The next part of the URL is what most people associate with a website and it's called the domain name. Have you ever asked yourself how your browser knows where to find a website? It happens because of the domain name.

This name is associated with a series of numbers called IP addresses on the internet. The fact that it is a name is a convenience for humans because it would be too hard to remember all of the numbers everytime we went to a website.

An IP address is like a phone number or zip code, it represents the physical location of the server on the internet. The names and numbers are stored through a sub-network inside the internet called DNS or Domain Name Servers. They act as an index or phone book of the names and IP addresses.

Think of DNS servers as the Post Office, by reading the zip code, they know the part of the country you live in and can route the mail to the appropriate location.

---

## Top Level Domains

<small>https://www.youtube. **com** /watch?v=MspVCc0_R3g&t=37s#top</small>


- [Domain type](https://en.wikipedia.org/wiki/List_of_Internet_top-level_domains)
- .com, .net, org, .gov, .edu
- Country specific [Monopo.ly](http://Monopo.ly)   [Instagr.am](http://instagr.am)
- Very flexible today

> > Author's Notes

The next part is the TLD or Top Level Domain. It represents the domain type and is supposed to identify the type of domain that you're using.

The most common types are .com for companies, .net for internet service providers, .org for non-profit entities, .gov for government organizations and .edu for educational organizations. In reality the requirement that the TLDs match function hasn't been enforced and has been removed. .com is by far the most common and most people will try to use a .com TLD before they use anything else.

In addition to that every country as assigned it's own TLD. Those are usually two letters long, so for example .co is for colombia, .ly is for lybia and .am is for amsterdam. A lot of people use these to make interesting URLs, so for example many tech companies use the .io (British Indian Ocean Territory) TLD for web applications like atom.io. Most of the time country specific TLDs are a bit more expensive.

In recent years, the amount of TLDs has exploded into many other categories, which include things like .dad, .biz, .info, .mobi, etc.

---

## Port Number
<small>https://www.youtube.com **:8707** /watch?v=MspVCc0_R3g&t=37s#top</small>

- A way to divide app requests
- Request sent through ports

> > Author's Notes

Another thing you might see on a URL as a way to further divide app requests is something called a [port number](https://en.wikipedia.org/wiki/List_of_TCP_and_UDP_port_numbers) It follows the TLD and starts with a colon and has a number.

Think of this as channels on radio or TV. They allow you to send different types of information on the same domain or subdomain. When you request web pages, they are sent through one of these channels, although most of the time you won't see these or deal with them. You may see these when setting up FTP, mail or some advanced web projects.

---

## Path
<small>https://www.youtube.com **/watch** ?v=MspVCc0_R3g&t=37s#top</small>

- The App, page, file or service you want
- Often a folder/file structure
- Can be data passed

> > Author's Notes

Next is the path of the request. This is separated by slashes `/` and let the server know the location of the service you're requesting. They can be setup in a couple of ways.

One way is to set it up to represent the directory location of the file you need. So for example, we could assume that `watch` specified in a youtube request represents the name of a folder in the server hosting the google application. If there was a file called video.mp4 then the path might be `/watch/video.mp4`.

This isn't the way YouTube or some other service works though, they use the PATHS as information passed to the server. The current way of managing URLs can also be written like this:

[https://www.youtube.com/watch?v=MspVCc0_R3g&t=37s#top](https://www.youtube.com/watch?v=MspVCc0_R3g&t=37s#top)

---

## Query/Parameters

<small>https://www.youtube.com/watch **?v=MspVCc0_R3g&t=37s** #top</small>


- Information to pass
- Name/Value Pairs

> > Author's Notes

The next part of the URL are called query/parameters. You can use the URL to pass detailed information to the server. Sometimes this data is passed in different ways and query parameters is a common way to do this.

The query starts with a question mark and you can then add a series of variables an equal sign `=` and then each name/value pair separated by an ampersand `&`. In the case of our video request, we're passing along the video ID in the `v` variable and and then the timecode using the `t` variable.

---

## Fragments

<small>https://www.youtube.com/watch?v=MspVCc0_R3g&t=37s **#top**</small>

- Subordinate resource
- ID inside page
- query/parameters

> > Author's Notes

A fragment is another way to pass information through a URL. It refers to a resource that is inside another resource. It' used in a couple of ways on pages.

You'll often see this used inside a page to refer to another section of the same page with a specific ID. So if you go to the [grid page](getbootstrap.com/docs/4.0/layout/grid/) in the Bootstrap Documentation, you'll see the normal documentation for the grid website, but if you want to read the documentation on [grid alignment](http://getbootstrap.com/docs/4.0/layout/grid/#alignment), you add a # and then the name of the section of the page you want to go to.

Sometimes the fragments are used more like query/parameters, it depends on how the server is set up to handle URLs.
