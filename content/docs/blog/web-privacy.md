---
title: "Web Privacy"
draft: true
tags:
- article
- guide
- privacy
- web
---

# A Guide to Web Privacy

## TL;DR

### Avoid

- Closed-source services with broad access to your browsing/personal data.
- Connecting to public wifi the internet without a VPN
- Gulag and Micro$oft
  - Particularly avoid Chrome & Gmail

### Use

- Firefox + Decentraleyes, uBlock Origin, multi-account containers
  - see post on post on [Internet Hygiene]({{< relref internet-hygiene.md >}})
- A paid, trusted VPN
- Use, install, or just understand the workings of Tor
- Email & cloud storage services like Protonmail
  - not owned by Gulag or M$,
  - located in Switzerland/France/Germany
  - where 'ENCRYPTION' is plastered all over their website

## Reasons Why

- The UK is a member of various surveillance coalitions: https://restoreprivacy.com/5-eyes-9-eyes-14-eyes/
- See the Snoopers Charter:
    - ISPs are required to track and store your browsing data.
            - At most (apparently), limited to device (MAC address), connection (IP: local and geoIP), connected server IP - addresses (but no packet introspection - i.e., 'www.reddit.com' but not any sub-URLs)
        - 23 different gov depts can request access for basically any reason at any level
        - It is simply a confirmation of what everyone knew was going on already.
            - It provides a surface-deep defence in the name of 'intelligence service oversight' via the Investigatory Powers Commission
    - This has some decent articles: https://restoreprivacy.com/
    - Ultimately, a VPN or Tor connection is only as safe as the powers which govern the land the server rests on.
        - It's possible to encrypt your traffic, but this makes browsing a chore
        - It's recommended to use services based in countries which believe in privacy, or at least have fairly robust laws governing who has access to personally-identifiable data - for the former, Switzerland (i.e. Protonmail), the latter, Germany.
    - There are a vast number of different techniques for tracking users across websites. Firefox + some add-ons can defend against 99% of these:
        - Addons/tools:
            - Decentraleyes
            - uBlock Origin (NOT plain uBlock or Adblock - these are now commercial entities/closed-source and there's no way to know what they do with your browsing data)
            - Firefox multi-account containers
        - You can go further with this (editing Firefox config options not exposed in the usual menu) and so on and so forth but it's really unnecessary.
            - Disabling remote fonts (i.e. Google) will make websites less pretty but removes a major avenue of fingerprint data.
            - The only way to fully avoid all this stuff is to opt-out of the good things (like disabling JavaScript on every website...)
        - A note on uBlock Origin:
            - You can make your browsing experience WAY better by using the 'element zapper/picker' tool.
                - Delete irritating/addictive website components (for example on imgur I have removed the '###right-content' section with viral images etc. Some people use it to delete the Facebook wall/other attention-capture mechanisms.)
        - Another options is hosts modification, which essentially provides your computer a 'banlist' of domains which it will never accept a connection to. This can range from ads to malicious sites to pr0n. 
          - Trade-off is occasional irritation but safer & faster browsing
            - https://github.com/mitchellkrogza/Ultimate.Hosts.Blacklist


## Recommendations

In rough order of easy/powerful/good to ballache/'not quite there yet'/'no-one I know of uses it'

    VPN:
        I've got ipvanish, think there's room on my subscription for one more device?
        Free VPN providers are never to be trusted.
        https://thatoneprivacysite.net -> lists and ranks VPNs
        NordVPN is generally well received but I'm forever suspicious of 'establishment-approved' VPNs, call me paranoid...
    Browser:
        Switch from Chrome to Firefox
        Learn how Tor/the internet works and use Tor
    Password mgmt:
        Not super necessary but good at defending against the inevitable and innumerable occasions where a server holding your email address & some portion of your identity is attacked.
            See: https://haveibeenpwned.com/
        KeePass is considered the best
    Searching: Use Qwant/duckduckgo
        Every alternative is a 'meta-search' engine sourcing results from Gulag/Bing, simply obscuring your identity with theirs
            Oh except these guys: https://www.mojeek.com/
                Unfortunately it's crap
        You can always use Google within Tor
    Cloud file storage:
        https://tresorit.com/
        Dropbox, Drive, OneDrive all include unlimited scanning and searching of your data in their ToS.
    Email providers:
        https://posteo.de/en
        https://tutanota.com/
        https://runbox.com/
        Mostly paid (limited free versions), but in the topsy-turvy future closed or open-source & paid is >>> closed-source free...
    Note-taking:
        Standard Notes: https://standardnotes.org/
            Apparently very nice iOS app
            Encrypted cloud storage (server admin has zero plausible access)
            Paid version/sub is kinda expensive though
    Online office: https://cryptpad.fr/
    Maps alternative: https://www.openstreetmap.org/#map=5/54.910/-3.432
        There's an iOS version
    Chat/socials:
        Telegram and Signal are good alternatives to Whatsapp
