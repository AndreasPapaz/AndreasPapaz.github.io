---
layout: about
title: about
permalink: /
subtitle: <a href='#'>See my Work</a>. 

profile:
  align: right
  image: prof_pic.jpg
  image_circular: false # crops the image to make it circular
  more_info: >
    <h3>Andreas Papazafeiropoulos</h3>
    <p>Software Engineer</p>
    <p>University of Illinois - Urbana-Champaign Alum</p>
    <p>Dad</p>
    <p>English/Greek</p>
    <p>Chicago</p>

selected_papers: true # includes a list of papers marked as "selected={true}"
social: false # includes social icons at the bottom of the page

announcements:
  enabled: true # includes a list of news items
  scrollable: true # adds a vertical scroll bar if there are more than 3 news items
  limit: 5 # leave blank to include all the news in the `_news` folder

latest_posts:
  enabled: true
  scrollable: true # adds a vertical scroll bar if there are more than 3 new posts items
  limit: 3 # leave blank to include all the blog posts
---

> We have proposed a system for electronic transactions without relying on trust.
>
> — Satoshi Nakamoto
> “Bitcoin: A Peer-to-Peer Electronic Cash System”

<img src="../assets/img/JavaHumor.png" style="max-width: 400px"/>

I'm currently a `Tech Lead` at **Capital One**, working on systems that enable `tokenization` of issued credit cards by the bank.
Payment Technology is one of my favorite areas of software engineering.
Within Payment Technology you are exposed to multiple areas of computer science & technology such as:
- TCP/IP and SOCKET connections to communicate to banks via the `ISO8583` messaging standard
- Distributed systems
- Micro Service Application Architecture
- Transactional databases including Transaction Isolation Levels
- Database design
- Software Security from configurations, injection, Computer System representation of Data.
- Legacy Systems to process payments and the effort to modernize to keep up with a changing world of how people think about money.


There were some years I worked at `Zoom Video Communications`, owning the `Live Video experience` for the `Contact Center` product. If you ever used customer support over SMS and thought, can I just call this support agent now because it would be easier for me to describe, then this is the product that should excite you. My responsibility was to combine session channels when requested and move details over to those channels when prompted to provide a seamless experience for the Customer Support Agent and the End User. This is where I grew the most in the sense of `product engineer`. This required working with partners to gather requirements, meeting with internal teams who owned the native channels like Zoom Voice, Zoom Video, Zoom SMS to then build out a flow to provide to the client and front-end engineers with the Design team and bring the feature to the finish line. Take a look below as it was presented during the **2022 Zoomtopia Event**. The most important thing at Zoom was the ability to communicate ideas, flows, and objectives as fast as possible to keep competitive with the market.

### Contact Center Channel Switching Zoomtopia Demo!
<iframe width="560" height="315" src="https://www.youtube.com/embed/YdiZyvjzlqU?si=lggC_nuBkhBbkz9m&amp;start=5425" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

I left `Zoom` at the end of **2024**. The company has the market cornered in terms of Video Communication technology. Where I worked was, Contact Center. This left me hungry to grow again. My interest came back to payments. The payment product that software engineers provide is very different than something like Zoom Contact Center. We could be leaking water behind the scenes like most software eventually becomes with rapid innovation, but if the process did not work, the business partners would be furious, as they should be. 

In payments, we have a lot of partners and customers who rely on us. The partners (Payment Processors) like Adyen or Paylocity, The Merchants like Starbuck or Amazon Store, and you, the end user. Now when we use our credit/debit cards, we think of that as a bank. Rarely do I hear that it's a product outside of the financial world. We get credit card points, a balance, a limit, a place to store your capital. But when your credit card doesn't work, you might call your bank and spend the next 15 minutes trying to figure that out. But if you have screaming kids and you're tired, you'll just use a different credit card and figure out the issue later.


When you are leading an engineering scrum team, the goal for the engineers is to follow the Story, meet the acceptance criteria, ensure the code coverage defined by team is met, then demo. After that, we don't really see our customers using the product. Leading the team who is an entry point for `tokenization` we have more insight, but a team that is responsible for `PAR` (Payment Account Reference) to map to `PAN`, the customers Payment Account Number, we are dealing with a different objective. What I do is ensure those details are communicated. For example, in distributed systems, it's important that we validate our data (sanitize input and sanitize output) to ensure that garbage in does not equal garbage out. If we have a critical `number` we must provide to our Partners, think paypal because they will manage the customers credit card on their platform. How would you think of our credit card number?

<img src="../assets/img/credit_card.jpg" style="max-width: 600px"/>

Credit Card Number -> `541275000000005`
How would you represent this number as a Product Owner? What about as a Software Engineer?
Think of it this way. if i tell you to add 10 to your credit card number, you know what to do. you would take `541275000000005` + `10` to get `541275000000015`. What if i told you to add 10 to your name? In software we use **ASCII** code to represent numbers and Character Encodings. So, `10` in characters is `\n` and someone that deals with these encodings might assume that you want to add a new line (`\n`) to your name. 

But when we deal with computers we want to use Integers. so back to my point on bridging the gap for Product and Engineering, when a payment partner asks for the `last 4 pan`, the last four of your credit card number, they would expect you to give them `0005`. But if you are using a number in the computer sense of C++ or Java you might just give them back `5`. Then they are left wondering where the other three digits are and have no way of knowing what you are trying to give them.

In simple terms. What is the number `0005`? its just `5` no matter how many leading digits (characters) there are. But, `0005` can be a valid pin number, pan last 4, phone password. 

Imaging on your iPhone your iOS code asks you to create a passcode and you enter `0007`, because you are James Bond of course. But when you try to unlock your phone you can't because the stored password now is represented as a number which would be `7`. So you figure this out and type `7` and your iphone now is expecting at the least 3 more digits. 


To wrap it up and cut it short because I would love to talk (or type) your ear (or eyes) off talking about how important payments are, this is the engine that enables people to live. I think about the ability to move around in the world directly connected to how you are able to move money.

<img src="../assets/img/vytina.jpg" style="max-width: 400px"/>

My Grandfather had to leave his home in Garea, Tripoli, Greece in 1941 at the age of 16. He landed in Toronto Canada, much like a lot of immigrants, with nothing but his 5 brothers. Those years leading up to where i am today, they ran restaurants and bars. I grew up in the restaurant industry and collecting payments, seeing how they evolve has been the lifeblood of my family. If the payment was fraudulent, delayed, then we might be in a bind. When we would go back to Greece in the 1990's we left Chicago with only the Cash we had on hand. 

Today, i can leave Chicago and visit my Yiayia in the mountains of Vytina Greece with only my Digital Credit Cards loaded into Apple Pay. 


<style>
img.standard-img {
    max-width: 100%;
    height: auto;
    border: 1px solid #ccc;
}
</style>
