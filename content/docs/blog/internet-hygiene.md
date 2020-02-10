---
title: "Internet Hygiene"
draft: true
tags:
- article
- guide
- health
- web
---

# A simple guide to keeping your Internet-use lean and hygienic

{{< hint info >}}
Social media companies hate him! 😄
{{< /hint >}}

If you need convincing of the reasons to tweak and clean up your internet usage, take a look at my post on the [economics of attention]({{< relref attention-economics.md >}})

## Changing usage patterns

TODO: create a table?

- Twitter
- Facebook
- YouTube
- Reddit

## Browser choice & add-ons

- Firefox
  - Leechblock
    - Blacklist, greylist, tweak whitelist
  - uBlock Origin
    - Element picker/zapper is god
  - YouTube Watchmarker
    - Don't get duped by YouTube recommendations - yeah, you have watched that video before!
  - Mind The Time
  - (that adblocker that fake-clicks on ads for you lol)
- Chrome
  - ?
- Brave

### Firefox mobile & sync

## Hosts

- Windows
- Mac
- Linux

## DNS & VPN

- Pi-Hole

## Router settings

- Periodically ban devices by MAC address

## uBlock Origin

Edit and clean up this:

    Click the uBlock menu icon
    Select the “element picker” tool. (it looks like an eye dropper)
    Mouseover the page until I’ve “selected” the portion of the page I want to remove. (uBlock highlights the current page node that the rule would apply to)
    Click that element of the page
    When I click, a very hard-to-see menu pops up in the bottom right corner of the page. I then move my mouse over to it, and click the “create” button.

At that point, uBlock finds that element of the page and deletes it. Forever.

A brief technical aside of what’s going on:

The page is represented to the user as a continuous document, but the underlying structure is a “Document Object Model”, and every page element is a “node” that exists mostly-independently of any other node on the page. We’re using uBlock to highlight the nodes of the DOM, and when we select one, uBlock says “ok, this here node… I’ll just remove it from the DOM”.

Lets remove more nodes. I really don’t like email/subscribe popups, so I always delete them.

remove the subscribe notification

gif of removing subscribe popup

“Trending” news is just a way of saying

    you’re not here to read these articles, but other people are clicking on them and we hope you’ll do the same.

So, remove it:

remove the sidebar

gif of removing the sidebar

The final version is quite a bit more peaceful and less disruptive and attention-grabbing than the origional website.

Oh, and these rules usually apply to “promoted” content that’s inserted in your “feed”. Just find the promoted node, select it, and delete it. This usually will apply to all promoted posts in your feed, so it’s a great way to get spam out of whatever long list you are scrolling through. (Facebook/Instagram/Twitter).
A few surprises that can happen with uBlock

Since uBlock by default disables many unwanted scripts and resources, it can introduce some unexpected behavior on websites. If a website isn’t behaving exactly as expected, turn off uBlock and see if the resource loads.

For example, some websites use untrustworthy javascript redirects to track your movement to third-party websites. if those redirects rely on untrusted third-party resources, they won’t be loaded on the page. Ditto for some kinds of form submission behavior, image/video resources, etc.

So, turning off uBlock is very easy:

    Click the uBlock menu icon
    click the blue “power” icon
    Click the “refresh page” button

uBlock will not block anything on this page now. To turn it back on, repeat the above steps.

turning off ublock

gif of temporarily disabling uBlock

If you accidentally delete an element you didn’t intend (like, the main content of the page, for example!) you’ll have to remove the “page rule” you just created.

This is very easy.

deleting wrong element

picture of where the article is *supposed* to be

    click uBlock menu icon
    click “open the dashboard”
    navigate to the “my filters” tab
    delete the bottom line from that list of rules. A line beginning with ! is a comment describing the next line, which is the “rule” that uBlock actually reads and applies to the page.
    click “apply changes”
    go back to the website (it’s tab is still open) and refresh the page.

fixing a bad delete

gif of removing the bad page rule

    OK, Josh, this is a lot of work to individually delete page nodes just to “preserve” my attention? I can read articles without worrying about the rest of the sidebars. Don’t you think this is overkill?

I don’t think it’s overkill.

A while back, I wrote about a book called Deep Work, and the profound impact it had on me. I stepped off of social media completely, and made efforts to trim away other distractions in my life.

Since taking these steps, I’ve become sensitive and more attuned to when I’m subjected to unwilling sources of distraction. It’s as if my “someone is trying to influence me” radar got much stronger.

I suspect that if you start using uBlock to remove annoying elements from pages, you’ll start developing a stronger radar for when someone is trying to monetize your attention, and and then you’ll block those elements, but then become even more attuned to those unwanted influences, and then block them, and on and on.

It is worth pointing out that this very website is devoid of those sorts of elements I find annoying. No popups, no sidebar content, no click-baity headlines. I even removed Google Analytics. If you want to share one of these posts on social media, you have to do it the old school way. Copy and paste the URL into your platform of choice.

Note how clean the URL is: www.josh.works/post-title. Positively peaceful.

The only metric I pay attention to is email subscribers. Someone subscribing via email is basically the highest endorsement of trust I can imagine. I’m extremely judicious in subscribing to other people’s websites, so I value other people trusting me with their email address.
