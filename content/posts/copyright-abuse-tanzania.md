---
title: "Copyright trolls, inspect element, and the online abuse ecosystem"
tags: ["safety", "copyright", "abuse", "blag"]
date: 2021-12-21T11:52:00-05:00
draft: false
---

When you think of a state-sponsored online influence operation, you might picture large sprawling networks of high-follower accounts spreading disinformation. To give one canonical example, Russia's Internet Research Agency [impersonated](https://medium.com/dfrlab/how-a-russian-troll-fooled-america-80452a4806d1) the Tennessee GOP on Twitter in the lead-up to the 2016 election, amassing over 130,000 followers before being taken down.

But most social media abuse operations are different. In this post, I want to talk about a [fascinating campaign](https://twitter.com/shelbygrossman/status/1466395068080615426) conducted by a pro-Tanzanian government network on Twitter. This network abused copyright reporting mechanisms to silence activists with moderate success until Twitter caught on to their scheme.

None of their accounts amassed any significant following, nor did any of their tweets have any meaningful reach. But it was quite successful in (temporarily) silencing government criticism. How did they do it?

<div class="aside ~info content">
<p class="supra font-semibold">Two Important Disclaimers ⚖️</p>
<p class="text-sm">First, I can't attribute this operation to the Tanzanian government itself. For all I know, this operation could have been run by individuals who just really wanted to stifle government criticism.</p>
<p class="text-sm">Second, I'm writing this post in my individual capacity. Although I played a (small) role in investigating this network at the Stanford Internet Observatory, this post is my own. If I get something wrong, that's my problem &mdash; not theirs.</p>
</div>

The operation itself was quite simple. Here's how it worked:

1.  The operatives found some accounts they wanted taken down. Maybe they wanted to take down the accounts because they criticized the Tanzanian government; maybe they just wanted to harass some activists.

2.  They copied tweets from those accounts onto a WordPress website as new posts, which they manually backdated to before the tweet was published. That way, it would look like their versions came first. (Perhaps you can see where this is going.)

3.  They submitted a copyright violation complaint to Twitter, claiming that the original author had copied *them*. Not recognizing the abuse, Twitter then took down the original posts. In two more extreme cases, Twitter even suspended activists' accounts. (To Twitter's credit, they've handled this really well: once they learned about the scheme, they restored the accounts and referred the network to us at the [Stanford Internet Observatory](https://io.stanford.edu) to investigate.)

If you're interested in learning more about this network, you can read the Internet Observatory's [official report](https://github.com/stanfordio/publications/blob/main/20211202-tz-twitter-takedown.pdf) and this [great Twitter thread](https://twitter.com/shelbygrossman/status/1466395068080615426).

What makes this operation interesting to me? Two things. First, it didn't involve "content" or "reach" in any traditional sense, challenging the typical conception of a coordinated abuse operation (usually, what you see in the news are disinformation campaigns). Second, the network was hilariously amateurish, which made it trivial to uncover and document their scheme.

## Online abuse ≠ disinformation

I think it's important that we don't adopt a myopic picture of coordinated social media abuse. Disinformation isn't the only problem. I'm relatively new to studying the online abuse ecosystem, and it hasn't taken me long to learn that there's no end to the creative ways that people can cause harm online.

Every feature is a potential vector for abuse. In the case of this pro-Tanzanian government network, that vector was copyright reporting mechanisms required under the U.S.'s Digital Millennium Copyright Act. The network reported false copyright violations to Twitter, pushing Twitter to suspend the accounts.

"Adversarial reporting" is a tactic by which a network of accounts all "report" an account for violating platform policies in an attempt to get it suspended. The ability to "report" an account is intended to be a way to prevent abuse. Like all features, though, it can be misused.

Adversarial reporting is deceptively common. In August 2020, Facebook suspended a [network of accounts](https://cyber.fsi.stanford.edu/io/news/reporting-duty) that used adversarial reporting to silence critics of Islam and the Pakistani government. In December 2021, Facebook [announced](https://about.fb.com/wp-content/uploads/2021/12/Metas-Adversarial-Threat-Report.pdf) they took down a network in Vietnam that also used adversarial reporting.

But despite the prevalence and impact of adversarial mass reporting, it's not a particularly well-known tactic outside the communities affected by it. It doesn't get the same sort of coverage that, say, disinformation campaigns get. That's understandable---a far-reaching disinformation campaign directly affects more people---but the consequences of a targeted reporting attack are still severe. This pro-Tanzanian government operation caused Twitter to suspend two high-profile activists.

## Influence sans content or reach

Let's unpack the differences between disinformation and targeted "mass reporting" operations a bit further. I think that understanding their fundamental distinction is important for anyone who wants to prevent, detect, and fight online abuse.

Abusive social media operations often involve *spreading* content of some sort---misleading or hateful content, for example. This particular operation attempted to *suppress* content, and yet it's still absolutely an abusive operation.

And yet it's very much not *disinformation*---at least not to me. While I'm not going to attempt to define disinformation, I think most agree that content plays an important role. Misleading state-sponsored propaganda probably qualifies; pervasive state censorship probably doesn't qualify.

Camille François at Graphika has a [useful framework](https://science.house.gov/imo/media/doc/Francois%20Addendum%20to%20Testimony%20-%20ABC_Framework_2019_Sept_2019.pdf) for characterizing disinformation. She argues that "viral deception" typically has three parts: "manipulative actors, deceptive behaviors, [and] harmful content." While this framework is certainly not one-size-fits-all, I think it helps clarify the difference between this particular operation and disinformation. It certainly involves manipulative actors and deceptive behaviors, but there isn't really any harmful content. (Or at least not in the part of the network I'm talking about.)

Content plays a central role in some operations, but not all. Indeed, content-based approaches for detecting abuse would miss this network entirely. Sometimes it feels like everyone is working on shiny ML-based models to detect "bad content" online, and while this is important and impactful work, "bad content" is only a small slice of the online abuse ecosystem.

Moreover, this network successfully suppressed the activists' posts without any meaningful reach. Each Twitter account in the network account had an average of nine followers, and 166 had no followers at all. Unlike more traditional content-based operations, adversarial copyright reporting doesn't require massive reach to be successful.

At this point I should note that it's not entirely correct to say that the network did not produce any content. The false copyright claims were only one part of the operation; the other part involved the operatives replying to activists tweets with (often childish) spam and harassment. (In one case, they told an activist they had an "empty head.") Still, the central component of this operation was the adversarial reporting.

## A global governance detour

As an aside, it's interesting to me that  *pro-Tanzanian government* operators attempted to silence *Tanzanian* activists using an *American* law. Why are Tanzanians subject to American regulations online?

Yes, sure, there are some obvious answers. Twitter is an American platform, and there are international copyright regulations (which I will not claim I understand). And it's probably easier for Twitter to just maintain one global copyright violation reporting policy, rather than handling everything on a region-by-region basis.

But I don't think these are satisfying answers. This question of global governance is so important that it'll get its own post some day---there's no way I can do it justice here. For now, it's just something to think about.

## Amateurish mistakes

The second component of this network that makes it interesting is just how amateurish it was, which made it easy for us to uncover exactly how the operation worked. I wrote an entire [Twitter thread](https://twitter.com/MilesMcCain/status/1466501157254144001) on this, and I'm expanding on it here.

Recall that this operation worked by copying activists' tweets, posting them on a WordPress site, then spoofing the publication date to predate the tweet. Then, they submitted a DMCA copyright complaint to Twitter. Since it looked like their spoofed version came first, Twitter took down the tweets.

How do we know they spoofed the dates on the posts? Well, the network's operators didn't know how to *actually* spoof dates, so they left a trail of evidence in the pages' metadata. They didn't realize their WordPress site also embedded the *last update time* in the source code of each page through invisible `<time>` HTML tags.

When we compared the claimed publication of the posts to the actual modification date, their scheme became clear. On one page, the publication date was 2:19 pm on Sep 27. The last updated date was 2:21 pm on Oct 2. Why are the times so similar? They created the page at 2:19 pm on Oct 2. Then, they manually set the date back to Sep 27---but they didn't bother to change the hour/minute fields. (Or they just didn't notice.) Then they inserted the activists' tweets into the post, and clicked "save" two minutes later.

With just these two timestamps, we could confidently say the dates were spoofed. There's nothing special about what we did here. It really was as simple as clicking "inspect element." (And despite what the Governor of Missouri might [claim](https://www.nytimes.com/2021/10/15/us/missouri-st-louis-post-teachers-hack.html), that's not very advanced!) But even simple techniques like this one can be incredibly revealing.

## Okay, so what?

This network certainly wasn't particularly sophisticated, nor was it particularly far-reaching. But I think it challenges the popular conception of what coordinated online abuse looks like. It wasn't a disinformation network---it didn't really produce *content* at all---but it was still very much "coordinated inauthentic behavior." Everyone working to fight abuse online should be mindful of the many different ways platforms can be used to cause harm. Disinformation isn't everything.

But this network is also interesting because it's so... *absurd*? Perhaps they just assumed that no one would bother to look at the page source when investigating their copyright complaints. (For a while, this assumption was correct.) Or maybe they just didn't realize they were leaking so much revealing metadata. Either way, this operation's execution was quite amateurish. Don't underestimate the power of "inspect element"!

> This post only talks about a small part of the operation, so be sure to read [our report](https://github.com/stanfordio/publications/raw/main/20211202-tz-twitter-takedown.pdf) to get the full picture. Thank you to everyone who provided feedback on earlier versions of this post.