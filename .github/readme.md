# Obsidian Templater Converters


## Description
[Obsidian](https://obsidian.md) is a cross-platform application that is popular in the personal knowledge management (PKM) space. It provides a rich environment in which to create interrelated and interlinked content. Much of this richness comes from the breadth of its community-driven plugin ecosystem. One of the most popular and powerful plugins is [Templater](https://silentvoid13.github.io/Templater/), a plugin that allows you to create simple and sophisticated content with reduced effort.

Often this is used to prepare a note template in Obsidian, or to add a particular section of text. i.e. Templater is used to insert static or dynamic text into an Obsidian note.

However, Templater is also capable of utilising existing text in terms of insertion. Therefore it is possible to create Templater templates that allow you to do things such as process a text selection in some way, effectively carrying out a conversion.

This repository is a collection of Templater templates that enable you to carry out text processing tasks on selected text.


## Installation


### Prerequisites
1. You have installed and are running [Obsidian](https://obsidian.md).
2. You have installed [the Templater plugin for Obsidian](obsidian://show-plugin?id=templater-obsidian).


### Adding Obsidian Templater Converters
Templater templates are Markdown files utilising Templater's syntax and that are located in a particular part of the Obsidian vault.

With Templater installed, open Obsidian's *Settings* and navigate to the *Community Plugins* > *Templater* section. In here, you should see a field that specifies the location for Templater's templates.

<img src="https://raw.githubusercontent.com/sylumer/obsidian-templater-converters/main/assets/template_folder_location.png">

Navigate to this folder in your preferred file management application.

From this GitHub repository, you can download individual files, the entire repository as a ZIP file, or sync it locally using your favourite `git` client.

> [!TIP]
> - [**GitHub Docs:** Downloading Files from GitHub](https://blog.hubspot.com/website/download-from-github)
> - [**HubsSpot:** How to Download from GitHub: A Beginner's Guide](https://blog.hubspot.com/website/download-from-github)

With local copies of the files (in your download folder, local repo, etc.), copy any that you wish to use into your Templater templates folder, and rename the file if you wish to refer to the template by a particular name. Just ensure that you retain the `.md` file extension.

> [!TIP]
> If you have lots of Templater templates, using a good naming convention can help make them easier to find when using them, and using sub folders can help with managing the files outside of Obsidian. In this repository, you may note that all of the templates begin "X.". This segregates them from other templates, and in fact I use different identifiers like this for different types of templates - e.g. "M." is the prefix for the semi-populated meeting note templates I have for many of my regular meetings.


# Using Obsidian Templater Converter Templates
Most Templater templates are designed top insert/replace existing text. These templates modify existing content, specifically the text selection. To use these templates, you should therefore select the text you want the template to process.

Any selection should include the whole line if you want to process a whole line, and not simply part thereof. This is because the selection is passed to Templater, the template is run against that, and then returned. It only processes your selected text, so you should be accurate in your selection.


## Background
I am a huge advocate of the [Drafts](https://getdrafts.com) app, and I built a large library of Drafts actions (the [ThoughtAsylum Action Group for Drafts](https://www.thoughtasylum.com/tadpole/#action-group-suite)), which I recommend you check out if you also happen to be a Drafts user. If you are not a Drafts user, but own an iPhone, or iPad, I would highly recommend it as an option for efficiently capturing content on the go that can then be pushed to Obsidian.

A good number of the actions I created were for processing text, and I found myself missing some of this functionality when using Obsidian - particularly as I also use Obsidian on non-Apple Platforms, and Drafts is only available on Apple platforms.

Given the flexibility of Templater, it presented a natural solution to what I wanted to do, and so I created a set of conversion templates that I continue to add to.


## Licensing, About Related Resources, Etc.
Licensing I hope isn't the most exciting thing here, but it is still very important. This repo is building on top of other things, and it is important to formally acknowledge the work they have put in so this collection of what are effectively scripts can have any function whatsoever.

- [Obsidian Templater Converters is CoffeeWare](https://github.com/sylumer/scriptrunner/blob/main/.github/license.md) - the templates in this repository are free you to use to use and you can donate a coffee below if you would like to fuel more of the free stuff I share for others to make use of.
- Obsidian is the amazing writing platform that makes so many things possible. It is created by the team at [obsidian.md](https://obsidian.md/about) and we just love using it.
- Templater is the creation of SilentVoid13, and we would encourage you to visit [the Templater repo on GitHub](https://github.com/SilentVoid13/Templater) to learn more and support their work. It makes so many things easier to do in Obsidian, and without this plugin, this would be a rather empty repository.
- Title Case - The Title Case code is a *very* slightly modified version of [To Title Case 2.1](http://individed.com/code/to-title-case/), copyright of David Gouch and licensed under the MIT License. You will find this information repeated in the comments of its MD file too. You too can standardise your titles with this one!


## Donate
If you find these templates useful and want to say thanks, I'm always up for a coffee.

<a href="https://www.buymeacoffee.com/sylumer" target="_blank"><img src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" alt="Buy Me A Coffee" style="height: 60px !important;width: 217px !important;" ></a>
