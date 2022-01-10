# FAQ - Discord Asked Questions

---

## List of questions I see on Discord a lot.

This document is a start for me to keep track of questions I see on the zrips.net Discord server in the Jobs #help channel. Hopefully throughout 2022 I will be able to build a collection and slowly get some answers to these questions. If you think information is missing, by all means make a pull request and complete the information (I will most likely review it and probably merge it).

## Questions

Some questions I saw

### How can I have players join only X amount of jobs? 

In `generalConfig.yml` you can set a global value for the maximum amount of jobs a player can join. 
```yaml
# Maximum number of jobs a player can join.
# Use 0 for no maximum
# Keep in mind that jobs.max.[amount] will bypass this setting
max-jobs: 3
```
Note that they need the [permission](https://github.com/mrfdev/Jobs/blob/main/Resources/FAQ/Jobs-permissions.md) as well to even join any job.

### How can I have everybody join only X jobs, but allow another group to join even more?

Check the answer for this question first: `### How can I have players join only X amount of jobs? ` and then update your group permission to have a higher number:
```
jobs.max.5
```
e.g. `lp group VIP permission set jobs.max.5 true`

### Does it work on 1.18?

Yes, Jobs 5.0.1.0 or newer, with CMILib 1.1.0.7 or newer will work Minecraft 1.18.1 (made for Spigot and Paper)

### Is CMILib required? What is this?

Yes, CMILib is a library by zrips that all his plugins require, including Jobs-Reborn. It's free to download, and you do not have to buy CMI to use it. 

### The plugin doesn't start!

That sucks, but we need more info, does it say in the console (latest.log has this info as well) that the error message starts with 'missing dependancy, cmilib required, download it' ? If so, the reason is that there's a missing dependancy, the cmilib is required. You should download it.

### Can I get the source code and customize it?

Jobs-Reborn is open source, you can view the source code on Github here: https://github.com/Zrips/Jobs if you want you can clone it, and copmile it yourself. more info about that here: https://github.com/mrfdev/Jobs/blob/main/Resources/FAQ/Jobs-jar-files.md

### I have a bug, fix it!

Yeah, life is not that easy, we deal in bug reports, not magic shows. So we will need more information. Please check that you're on the latest build of your service engine; type: `/ver` and see how far behind you are. Additionally, get the latest CMILib jar from spigotmc, and the latest Jobs .jar from spigotmc. Try again. If it still fails, check the latest.log file to see what the errors are during startup and resolve those. If you believe you've found a bug, gather up the info about your server and go to zrips's github and submit a new issue for review. Explain what the issue is, how to reproduce it. What you've done to mitigate it, what /ver and other versions you have of what you're trying to work with and include the full error message.

### Jobs is lagging my server, shows in timings report.

This is a loaded question, because it can mean a lot of things. Another plugin can hang the main thread, forcing a queue to build up or other tasks to wait before they can complete. We will need to know much more information. Including a timings report. Github > new issue > is the best way to deal with that. Think about it first what info will be helpful to help you the best.

### What are the official sites?

- Jobs-Reborn on SpigotMC ; https://www.spigotmc.org/resources/jobs-reborn.4216/

- CMILib jar on SpigotMC ; https://www.spigotmc.org/resources/cmilib.87610/

- Bug reports on Github ; https://github.com/Zrips/Jobs/issues

- Source code on Github ; https://github.com/Zrips/Jobs/

- Jobs Documenation on Zrips.net ; https://www.zrips.net/jobs/

- Zrips Discord ; https://discord.gg/dDMamN4

### What are the placeholders for Jobs plugin?

In the console, type: `jobs placeholders` to get the full list.

### I asked a question and I am getting ignored?

To get the best help you can get we need information, then zrips on Github, or the community members on Discord can help you better.

- Have some patience. Post the question, provide info, and just wait.
- We always advice to stay current and make frequent backups!
- Provide the information if you can (console commands):

**# Server engine:** `ver`
**# Plugin details:** `jobs version`
**# CMI-Library:** `ver CMILib`
**# Vault version:** `ver Vault`
**# Economy manager:** `ver CMI`
**# Permission Manager:** `ver LuckPerms`

- Also keep an eye on the console/logs, to make sure you spot any console errors during startup of any plugins, and/or when you try to do something with this plugin. If you want to paste your big error msgs, please use a pastebin like service like <https://paste.md-5.net/>


### Jobs Economy

<https://github.com/mrfdev/Jobs/blob/main/Resources/FAQ/Jobs-economy.md>

More Economy info <https://ptb.discord.com/channels/452792793631555594/526402919826849804/688267075818750053>

### Helping Translate Jobs

<https://ptb.discord.com/channels/452792793631555594/526402919826849804/611253737033302031>

### Jobs Points Explained 

<https://ptb.discord.com/channels/452792793631555594/526402919826849804/803721132984631296>

### Jobs/ files Explained

<https://ptb.discord.com/channels/452792793631555594/526402919826849804/809103176421736469>

### Jobs Permissions

<https://www.zrips.net/jobs/permissions/>

### Dynamic Signs

<https://www.zrips.net/jobs/signs/>

### Chat Titles

<https://www.zrips.net/jobs/chat-titles/>

### Common Issues

<https://www.zrips.net/jobs/common-issues/>

### Jobs API

<https://www.zrips.net/jobs/api/>

### Jobs GUI adjustment

<https://ptb.discord.com/channels/452792793631555594/526402919826849804/841708722367102997>

### How do I stop registring furnacs?

Short answer: I do not know, maybe the permission can be set to 0 ?

### Can I stop paying out in money? (or points or exp)

Yes, `generalConfig.yml` lets you enable/disable the three payout options. 

### People in creative mode are getting paid!

Make sure you're not an operator or that you did not `*` wildcard your permissions. You can also negate the permission specifically in the groups to not pay out in creative mode.

The check permissions page. And make sure the setting is disabled in generalConfig.yml

### How can I use (short) Jobs names (in chat, etc)

My best bet is to check the `/jobs placeholders` and find the one you want to use, and use that in your chat manager, holograms, etc. 

https://www.zrips.net/jobs/chat-titles/

```
chat-display
Display method of the title. Accepted values are full, title, job, shortfull, shorttitle, shortjob and none
```