# 🔫 Shoot the pet! Your workstation is a cattle.

`Pets vs. Cattle`. You probably heard that term before. In 2011-2012, *Randy Bias* ([@randybias](https://twitter.com/randybias)) was struggle to explain to customers how AWS, cloud native apps and cloud more generally was fundanmentally different what what had gone before. He coined the terms *pets* and *cattles* as the analogy to the disposability of cloud services and the uniqueness of monolith servers. Randy pitched the following:

> In the old way of doing things, we treat our servers like pets, for example Bob the mail server. If Bob goes down, it’s all hands on deck. The CEO can’t get his email and it’s the end of the world. In the new way, servers are numbered, like cattle in a herd. For example, www001 to www100. When one server goes down, it’s taken out back, shot, and replaced on the line.

Since then, the cattle model of operation has been evangelised as one true way for building a reliable, fault-tolerant infrastructure in cloud era. But there is one area where it is often neglected to apply the cattle mentality: our end-user computing space, ie. your desktops, laptops and workstations.

## Pets? Cattle? Why workstation is usually pet?

_Pets are unique_ and not easily replaced. Typical desktops, laptops and workstations are not disposable. You manually build, install, hand tune the environments on your desktop to your liking. If your devices break in some way, you will be less productive or even blocked from progressing with your work until it's fixed. The user applications and data need to be located and migrated when it is time to replace that device.

On other hand, _cattle are disposable_. Your work environment and user data are located safely off the physical machines or has been replicated. If you suffer a hardware failure, you can quickly log in to another workstation or continue where you left off. Alternatively, it is relatively trivial to spin up another workstation to get back to your work.

## Why should you care?

There are a number of motivation for us to move toward treating your workstation as cattle:

1. _[Your device might be seized by custom when travelling](https://www.theguardian.com/world/2018/aug/25/sydney-airport-seizure-of-phone-and-laptop-alarming-say-privacy-groups)_: Nathan Hague, a 46-year-old British-Australian software developer, has had his devices seized at Sydney Airport, and believes his laptop password cracked and his digital files inspected by Border Force officers. It is recommended that people who wanted to protect their data should not carry devices across international borders.
2. _Your device will eventually break_: as with all things in life, death is inevitable. Your devices *will* break. It is up to you to maintain an up to date backup of all your data. But have you ever setup a new computer and has a daunting realisation that you forgot an **very important** files you hide away in a directory somewhere?
3. _It works on my machine_ <sup>TM</sup>. A multitude of software and patches over the year on your workstation cause your apps to behave differently from production. Codifying your workstation as code ensure your environment is reproducable and ready to be ship to production.

## Turning pet to cattle

To turn pets to cattle, you need to decide on how to break your workstation into compostable, reproducable blocks:
1. _Storage_: how can I quickly move storage to another devices? Do I need to keep it in sync?
2. _Compute_: how can I quickly spin up a workstation with all applications and libraries that I use?
3. _Authentication_: how can I ensure it's my workstation I am replacing and someone cannot impersonate me?
4. _Metal_: if my machine breaks tomorrow, how quickly can I replace it? Can I work off something else?

