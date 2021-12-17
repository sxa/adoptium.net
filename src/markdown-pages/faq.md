---
path: "/faq"
title: "Frequently Asked Questions"
authors: gdams, karianna, sxa555, aahlenst, sxa, tellison, kemitix
---

We have completed our first releases at Eclipse Temurin and will be updating this FAQ as and when things are completed and available. If you want to talk to us or ask additional questions the best place is our [slack instance](https://adoptium.net/slack.html) or via an issue in the [support channel](https://github.com/adoptium/adoptium-support) if your question is not covered by one of the entries below.

## Where are the latest JDKs?

Most of the Eclipse Temurin builds with HotSpot for 8u312-b07, 11.0.13+8 and jdk-17.0.1+12 are now available on this site.

## What happened to AdoptOpenJDK?

Short answer: The project got so big that we chose to [move under the Eclipse Foundation](https://projects.eclipse.org/projects/adoptium) as [announced last year](https://blog.adoptopenjdk.net/2020/06/adoptopenjdk-to-join-the-eclipse-foundation/) to provide us some additional stability for the future!

Longer answer: The builds you know as AdoptOpenJDK are now "Eclipse Temurin by Adoptium" ([release blog post](https://blog.adoptium.net/2021/08/adoptium-celebrates-first-release/)) Don't worry though - despite the branding changes it is the same open build processes, AQAvit test suites and primarily the same team producing them as before, but there are [more larger companies](./members) now involved in the working group.

## Why doesn't the AdoptOpenJDK site redirect here?

Two reasons. Firstly: Since users are still transitioning we have left the old site working as it did before with the same layout and buttons as before. The links on the old site will give you the latest Temurin builds, but this should not be relied on and users should begin to migrate over to using the Adoptium API and website to download Temurin binaries. There are some variants which are not yet available at Adoptium, and these can [still be obtained](#will-the-migration-break-my-api-links) through the old site, so we are not removing the old site as this would result in some functionality disappearing with no warning. It's not ideal, and causes some SEO confusion, but we feel it is the right option for now. In the future the Adoptium web site will be more than just Temurin so a pure redirect at between the domains would not ba appropriate.

Secondly: As alluded to at the end of the previous paragraph, some things are not available at Adoptium.net and so a the old web site is retained without an explicit redirect in order to continue hosting them at present. This includes things like the [Upstream builds](https://adoptopenjdk.net/upstream.html) and [IcedTea-WEB](https://adoptopenjdk.net/icedtea-web.html). We would expect to get lots of complaints if this stuff just disappeared from view and that would not be the best option for our customers.

## What is this "Eclipse Temurin" name?

This is the project and brand name for the binaries that the Eclipse Foundation produces. You can think of these as the successor binaries to AdoptOpenJDK. However, it is important to note that these binaries are just one of many that will eventually be in the [Eclipse Adoptium Marketplace](https://github.com/adoptium/adoptium/issues/7). While we appreciate that the Adoptium/Temurin name split is more confusing that just “Adoptium”, this is similar to how other vendors brand their binaries, e.g. Amazon has Corretto, Azul has Zulu (and others). The “Adoptium” project and working group will deal with more than just Temurin so the distinction is important to maintain.

## Where are the OpenJ9 builds?

The transition to Adoptium means we have unfortunately not been able to continue to distribute builds of Eclipse OpenJ9. IBM has now taken them over and they are now available as "[IBM Semeru](https://developer.ibm.com/languages/java/semeru-runtimes/)". There is no need to be concerned about the change - it is still free.

## Where are the docker images?

Due to the limited amount of people we have working on the project, maintaining the wide variety of docker images that we provided from AdoptOpenJDK was becoming unsustainable. For that reason we are releasing a cut down set of docker images for Temurin. For those users who want a containerized Linux distribution that we don't provide an image for, use this guide.

## Where are the Linux rpm/deb packages?

We are working on a solution for that at the moment with [this issue](https://github.com/adoptium/installer/issues/330) as an umbrella for the work

## Why do the packages not include IcedTea-Web?

The agreements that we have since moving under the Eclipse Foundation mean that we can no longer include IcedTea-Web in our installers. However, you can still add the functionality if you require it using the [instructions here](https://blog.adoptopenjdk.net/2018/10/using-icedtea-web-browser-plug-in-with-adoptopenjdk/).

## Will the migration break my API links?

There is a [new download API](https://api.adoptium.net/q/swagger-ui/) provided by Adoptium for downloading Eclipse Temurin builds.

The good news is that it looks very like the AdoptOpenJDK one did so migration isn't too difficult for anyone currently using it.￼ At present the AdoptOpenJDK API will redirect to Temurin (or Semeru) if available when you request the latest release builds. We have done this because we haven't had time to encourage the community to fully migrate and because we haven't released everything yet so there are missing builds in the Adoptium API. Note that this will be a temporary measure and the AdoptOpenJDK API is not expected to be retained forever to do this although the timescale for removing the redirection is still to be decided.

## Can you give a talk on the project?

The people involved in the project are passionate about promoting it and we are keen to find ways to promote the work we do at Adoptium and with the Temurin binaries so feel free to get in touch with us if you have a forum you wish us to participate in and we will see what we can do. In general contacting the team via Slack is the best way to engage with us.