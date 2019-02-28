![Banner](https://raw.githubusercontent.com/sysgears/grain/master/banner.png)

[![Twitter Follow](https://img.shields.io/twitter/follow/grainframework.svg?style=social)](https://twitter.com/grainframework) [![Twitter Follow](https://img.shields.io/twitter/follow/sysgears.svg?style=social)](https://twitter.com/sysgears)

Grain is a lightweight framework and a very powerful static website generator written in Groovy to help make website
creation intuitive and enjoyable. Grain suits development of complex, static websites for companies and neat blogging
websites for personal use. The framework builds on [simple ideas](#documentation) and provides live reload to help you
rapidly develop custom [themes](#available-grain-themes).

## Documentation

All the Grain documentation is located in teh [`docs/General Docs.md`] file. You may learn more about using Grain in the
following sections:

* [IDE Integration]
* [Grain website structure]
* [Environments]
* [Advanced Grain configuration]
* [Page structure]
* [Layouts]
* [Includes]
* [URL and resource mapping]
* [Tag libraries]

## Key features

Grain comes with the following key features:

 - A preview mode that allows you to make changes and see them applied on the fly
 - Support for embedded Groovy code for any content files (stylesheets and JavaScript files)
 - Configurable conventions that allow you to process content sources using Groovy
 - Support for Markdown, reStructuredText, and AsciiDoctor
 - Compression and minification of source files
 - Code highlighting with Python Pygments
 - Built-in Sass and SCSS support
 
## Themes & templates

A Grain website project is called a _theme_, and Grain has a few developed responsive themes that you can use. Consult the list of pre-built Grain themes below:

* [Agency]
* [Business Casual]
* [Clean Blog]
* [Freelancer]
* [Grain Stylish Portfolio]
* [Grain Theme Template]
* [New Age]
* [Octopress]

## Getting started

### Requirements

To run a Grain project, you need to use [JDK 7 or later]. Download and install the appropriate JDK for your operating
system.

### Installation

Grain requires no installation. You only need to download one of the [themes](#available-grain-themes) and run the
project &mdash; Grain will be loaded automatically as a JAR dependency.

If you're new to Grain, we recommend that you start with the [Grain Octopress](#octopress) theme. It gives an overview
of how you can efficiently use most Grain features.

If you consider building a Grain website from scratch, try out the [Grain Theme Template](#grain-theme-template).

### Preview a Grain website

Navigate to the location of your newly created website and run the command below to launch the project in preview mode:

```bash
cd /path/to/your_site
./grainw
```

> Here and further the command-line snippets are provided only for the Unix-like operation systems. If you're running
Grain on Windows, use the `grainw` command instead of `./grainw`.

Once the project is built, you can visit your favorite browser at `http://localhost:4000` to view the website. You can
add, change, or delete website files and see all the changes in the browser immediately after refreshing the page.

### Generate and deploy

When you're ready to deploy your Grain-based website, you first need to generate all the website files by executing the
following command:

```bash
./grainw generate
```

The website files are generated into the `/path/to/your_site/target` directory.

You can deploy the website files either manually or with the help of Grain:

```bash
./grainw deploy
```

Check the [Deployment Configuration] section for more information.

## The Grain Community

There are many ways to get involved with the project:

- [Mailing List] - reach us or ask the community for help
- [Issue Tracker] - make Grain better by suggesting improvements
- [Twitter] - keep up with the latest Grain news and announcements

## Contributing

Any person or company wanting to contribute to Grain Framework should follow
the following rules in order to their contribution being accepted.

## Sign your work

We require that all contributors "sign-off" on their commits.  This certifies that the contribution is your original
work, or you have rights to submit it under the same license, or a compatible license.

Any contribution which contains commits that are not Signed-Off will not be accepted.

To sign off on a commit you simply use the `--signoff` or `-s` option when committing your changes to Git:

```
git commit -s -m "Adding a new widget driver for cogs."
```

This will automatically append the following data to your commit message:

```
Signed-off-by: Your Name <your@email.com>
```

By doing this, you certify the below:

```
Developer's Certificate of Origin 1.1
```

If you wish to sign-off commit messages for each commit without specifying `-s` or `--signoff` all the time, rename
`.git/hooks/commit-msg.sample` to `.git/hooks/commit-msg` and uncomment the following lines:

```sh
SOB=$(git var GIT_AUTHOR_IDENT | sed -n 's/^\(.*>\).*$/Signed-off-by: \1/p')
grep -qs "^$SOB" "$1" || echo "$SOB" >> "$1"
```

## Developer's Certificate of Origin

To help track the author of a patch as well as the submission chain,
and be clear that the developer has authority to submit a patch for
inclusion into this project please sign off your work.  The sign off
certifies the following:

    Developer's Certificate of Origin 1.1

    By making a contribution to the project, I certify that:

    (a) The contribution was created in whole or in part by me and I
        have the right to submit it under the open source license
        indicated in the file; or

    (b) The contribution is based upon previous work that, to the best
        of my knowledge, is covered under an appropriate open source
        license and I have the right under that license to submit that
        work with modifications, whether created in whole or in part
        by me, under the same open source license (unless I am
        permitted to submit under a different license), as indicated
        in the file; or

    (c) The contribution was provided directly to me by some other
        person who certified (a), (b) or (c) and I have not modified
        it.

    (d) I understand and agree that this project and the contribution
        are public and that a record of the contribution (including all
        personal information I submit with it, including my sign-off) is
        maintained indefinitely and may be redistributed consistent with
        this project or the open source license(s) involved.

    (e) I hereby grant to the project, SysGears, LLC and its successors; 
        and recipients of software distributed by the Project a perpetual,
        worldwide, non-exclusive, no-charge, royalty-free, irrevocable
        copyright license to reproduce, modify, prepare derivative works of,
        publicly display, publicly perform, sublicense, and distribute this
        contribution and such modifications and derivative works consistent
        with this Project, the open source license indicated in the previous
        work or other appropriate open source license specified by the Project
        and approved by the Open Source Initiative(OSI)
        at http://www.opensource.org.

## License

Grain is licensed under the [Apache License], Version 2.0.

[mailing list]: https://groups.google.com/forum/#!forum/grain-user
[Grain]: http://sysgears.com/grain/
[Apache License]: http://www.apache.org/licenses/LICENSE-2.0.html
[Developer's Certificate of Origin]: https://raw.github.com/sysgears/grain/master/DCO
[Issue Tracker]: https://github.com/sysgears/grain/issues
[Twitter]: http://twitter.com/grainframework
[deployment configuration]: https://github.com/sysgears/grain/blob/master/docs/latest.md#deployment-configuration
[`docs/General Docs.md`]: https://github.com/sysgears/grain/blob/master/docs/General%20Docs.md
[ide integration]: https://github.com/sysgears/grain/blob/master/docs/General%20Docs.md#ide-integration
[grain website structure]: https://github.com/sysgears/grain/blob/master/docs/General%20Docs.md#grain-website-structure
[environments]: https://github.com/sysgears/grain/blob/master/docs/General%20Docs.md#environments
[advanced grain configuration]: https://github.com/sysgears/grain/blob/master/docs/General%20Docs.md#advanced-grain-configuration
[page structure]: https://github.com/sysgears/grain/blob/master/docs/General%20Docs.md#page-structure
[layouts]: https://github.com/sysgears/grain/blob/master/docs/General%20Docs.md#layouts
[includes]: https://github.com/sysgears/grain/blob/master/docs/General%20Docs.md#includes
[url and resource mapping]: https://github.com/sysgears/grain/blob/master/docs/General%20Docs.md#url-and-resource-mapping
[tag libraries]: https://github.com/sysgears/grain/blob/master/docs/General%20Docs.md#tag-libraries
[agency]: https://github.com/sysgears/grain/blob/master/docs/Grain%20Themes.md#agency
[business casual]: https://github.com/sysgears/grain/blob/master/docs/Grain%20Themes.md#business-casual
[clean blog]: https://github.com/sysgears/grain/blob/master/docs/Grain%20Themes.md#clean-blog
[freelancer]: https://github.com/sysgears/grain/blob/master/docs/Grain%20Themes.md#freelancer
[grain stylish portfolio]: https://github.com/sysgears/grain/blob/master/docs/Grain%20Themes.md#grain-stylish-portfolio
[grain theme template]: https://github.com/sysgears/grain/blob/master/docs/Grain%20Themes.md#grain-theme-template
[new age]: https://github.com/sysgears/grain/blob/master/docs/Grain%20Themes.md#new-age
[octopress]: https://github.com/sysgears/grain/blob/master/docs/Grain%20Themes.md#octopress
[https://github.com/sysgears/grain-theme-new-age]: https://github.com/sysgears/grain-theme-new-age
[https://github.com/sysgears/grain-theme-clean-blog]: https://github.com/sysgears/grain-theme-clean-blog
[https://github.com/sysgears/grain-theme-octopress]: https://github.com/sysgears/grain-theme-octopress
[octopress]: http://octopress.org/docs/
[https://github.com/sysgears/grain-theme-template]: https://github.com/sysgears/grain-theme-template
[https://github.com/sysgears/grain-theme-portfolio]: https://github.com/sysgears/grain-theme-portfolio
[https://github.com/sysgears/grain-theme-freelancer]: https://github.com/sysgears/grain-theme-freelancer
[https://github.com/sysgears/grain-theme-agency]: https://github.com/sysgears/grain-theme-agency
[https://github.com/sysgears/grain-theme-business]: https://github.com/sysgears/grain-theme-business
[JDK 7 or later]: http://www.oracle.com/technetwork/java/javase/downloads/index.html
