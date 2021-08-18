# Licenses

## Introduction

### Section Overview

In this section, we will provide an overview of typical software licenses and why it is important to familiarize ourselves with them and specify them accurately.

### Learning Objectives

By the end of this section, you should be able to:

* Distinguish the main types of licenses used by software.
* Know sources for additional information on licenses you may be using, and attributes of those licenses.
* Explain how to refer to specific software licenses in your code.

## Licenses

### What Are Licenses?

According to [Wikipedia](https://en.wikipedia.org/wiki/Software_license):

> A software license is a legal instrument . . . governing the use or redistribution of software"

Let's break down this phrase and explore it a bit.

#### "Software"

*Software* refers to a document that represents a program or firmware written by an author. The author of the software can be one or many people, and possibly doing the work on behalf of a company. 

A software program is meant to create a machine executable version of an algorithm or idea. Many computer languages can be used to write the software, which will get compiled or interpreted into machine language.

#### "Legal instrument"

[Legal instrument](https://en.wikipedia.org/wiki/Legal_instrument) is a **legal** term that is used for any formally executed written document (such as a software program) that can be formally attributed to its author, that records and formally expresses a legally enforceable act, process, or contractual duty, obligation, or right, and therefore evidences that act, process, or agreement.

#### "Governing the use"

*Governing* the use describes how a person or company can use this software program. What is permitted and what is not? Can they publicly post it, use it inside their company or for personal use at home?

#### "Redistribution"

*Redistribution* describes how it can be shared. Can the person using it give a copy to a friend, modify or create derivative works, post online, etc.?

---

So, a license is a granting of rights from those producing the software to those who want to use it, regarding how it can be used and shared. It is a set of guidelines on the liabilities and responsibilities associated with using and distributing the software program.

![Licences division](img/licences-division.png)

The diagram shows there are two main types of software licenses. Those that are "proprietary" and those which are free software or open source. The terms under which a user may distribute or copy the software identifies which category it generally belongs in. 

Some software might be available to download for free, but if it is not provided under an open source license, then it is not open source software. In particular, if software is freely downloadable but doesn’t state any license, then it cannot be assumed to be "open source".

For simplicity - we will just refer to free software and open source licenses as "open source" in the rest of the course and we will refer to non-open source licenses as "proprietary".

### License Types

Most licenses fall into one of two broad categories: proprietary or open source.

#### Proprietary Licenses

Proprietary licenses are licenses where the copyright holder keeps many or most of the rights to themselves, and often adds additional restrictions on what users can do with the software. Proprietary licenses are specific to a company or a project.

Some proprietary software is commercial and you have to pay for a license to use it, but other proprietary software can be freely available.

It is important to read the terms of the proprietary license, and make sure you will be able to comply with it before incorporating the software associated with a license in your program. For example, some proprietary licenses require an explicit acknowledgement that you have read the license (sometimes called a click-through). **If you are not able to follow and understand the terms, do not use the code!**

#### Open Source Licenses

Open source licenses are generally understood to be those that follow the definition of open source developed by the [Open Source Initiative](https://opensource.org/) organization. They allow software to be freely used, modified, and shared.

Open source licenses are generally grouped as:

* **Permissive or Copyleft** - The license might impose few or no requirements on the licensee, permitting use and redistribution in proprietary applications. Or it might require redistributors to provide to downstream recipients the same freedoms they received for the upstream software, or for their own works derived from it or added to it.
* **Patent Grant or No Patent Grant** - A patent grant can either be explicitly specified, or implied by the text (called implicit). Or, there can be no patent grant associated with some licenses, which some may consider not to be open source licenses as a result. 

We will discuss these categories in more detail shortly.

---

To learn more about open source licenses, review the Open Source Initiative's website - ["Licenses & Standards"](https://opensource.org/licenses).

### Open Source Definition

For code to be considered open source, the license the code is released under should comply with the properties listed in the [Open Source Definition](https://opensource.org/osd-annotated) maintained by the [Open Source Initiative](https://opensource.org/) (OSI).

![Open Source Initiative logo](img/osi-logo.png)

The OSI logo is a registered trademark of Open Source Initiative. Source: [Wikipedia](https://en.wikipedia.org/wiki/Open_Source_Initiative), provided under [CC-BY-2.5](https://creativecommons.org/licenses/by/2.5/).

#### Free Redistribution

The license shall not restrict any party from selling or giving away the software as a component of an aggregate software distribution containing programs from several different sources. The license shall not require a royalty or other fee for such sale.

#### Source Code

The program must include source code, and must allow distribution in source code as well as compiled form. Where some form of a product is not distributed with source code, there must be a well-publicized means of obtaining the source code for no more than a reasonable reproduction cost preferably, downloading via the Internet without charge. The source code must be the preferred form in which a programmer would modify the program. Deliberately obfuscated source code is not allowed. Intermediate forms such as the output of a preprocessor or translator are not allowed.

#### Derived Works

The license must allow modifications and derived works, and must allow them to be distributed under the same terms as the license of the original software.

#### Integrity of the Author's Source Code

The license may restrict source-code from being distributed in modified form only if the license allows the distribution of "patch files" with the source code for the purpose of modifying the program at build time. The license must explicitly permit distribution of software built from modified source code. The license may require derived works to carry a different name or version number from the original software.

#### No Discrimination Against Persons or Groups

The license must not discriminate against any person or group of persons.

#### No Discrimination Against Fields of Endeavor

The license must not restrict anyone from making use of the program in a specific field of endeavor. For example, it may not restrict the program from being used in a business, or from being used for genetic research.

#### Distribution of License

The rights attached to the program must apply to all to whom the program is redistributed without the need for execution of an additional license by those parties.

#### License Must Not Be Specific to a Product

The rights attached to the program must not depend on the program's being part of a particular software distribution. If the program is extracted from that distribution and used or distributed within the terms of the program's license, all parties to whom the program is redistributed should have the same rights as those that are granted in conjunction with the original software distribution.

#### License Must Not Restrict Other Software

The license must not place restrictions on other software that is distributed along with the licensed software. For example, the license must not insist that all other programs distributed on the same medium must be open-source software.

#### License Must Be Technology-Neutral

No provision of the license may be predicated on any individual technology or style of interface.

---

Whether a license complies with the definition, and therefore is listed on OSI's [approved open source license list](https://opensource.org/licenses/category), is determined by OSI through their [license review process](https://opensource.org/approval).

### Permissive or Copyleft License?

**Permissive licenses** are those with minimal requirements on what you must do when redistributing the software. Those requirements are typically limited to things like retaining or delivering attribution notices. Because requirements are minimal, it is often easier for permissively-licensed software to be combined with copyleft and/or proprietary software, but there are compatibility issues in some cases. The ["Permissive Software License"](https://en.wikipedia.org/wiki/Permissive_software_license) article on Wikipedia gives much more detail on this, including a compatibility diagram between the classes of licenses (the topic of compatibility between licenses is not covered in this course).

Common examples of permissive licenses are: 

* [MIT](https://spdx.org/licenses/MIT.html)
* [BSD-2-Clause](https://spdx.org/licenses/BSD-2-Clause.html) and [BSD-3-Clause](https://spdx.org/licenses/BSD-3-Clause.html)
* [Apache-2.0](https://spdx.org/licenses/Apache-2.0.html)

**Copyleft licenses** are sometimes called protective or reciprocal licenses. The term copyleft originated from the GNU licenses, but has been expanded over time to cover other licenses. Copyleft licenses have requirements for how the software can be redistributed, as well as requirements that may impact how derivative works can be distributed.

These licenses tend to get grouped into **strong and weak copyleft licenses**. 

From the ["Copyleft"](https://en.wikipedia.org/wiki/Copyleft) Wikipedia article, we find the following useful definitions:

> "Weak copyleft" refers to licenses where not all derived works inherit the copyleft license; whether a derived work inherits or not often depends on the manner in which it was derived. "Weak copyleft" licenses are generally used for the creation of [software libraries](https://en.wikipedia.org/wiki/Library_(computing)), to allow other software to link to the library, and then be redistributed without the legal requirement for the work to be distributed under the library's copyleft license.

Examples of the "weak copyleft" licenses are: 

* Lesser GNU Public License (written as [LGPL-2.0](https://spdx.org/licenses/LGPL-2.0.html), [LGPL-2.1](https://spdx.org/licenses/LGPL-2.1.html) or [LGPL-3.0](https://spdx.org/licenses/LGPL-3.0.html))
* Mozilla Public Licenses (written as [MPL-1.0](https://spdx.org/licenses/MPL-1.0.html), [MPL-1.1](https://spdx.org/licenses/MPL-1.1.html) or [MPL-2.0](https://spdx.org/licenses/MPL-2.0.html))
* Eclipse Public License (written as [EPL-1.0](https://spdx.org/licenses/EPL-1.0.html) or [EPL-2.0](https://spdx.org/licenses/EPL-2.0.html))
* Common Development and Distribution License (written as [CDDL-1.0](https://spdx.org/licenses/CDDL-1.0.html) or [CDDL-1.1](https://spdx.org/licenses/CDDL-1.1.html))

> "Strong copyleft" refers to the class of licenses which specify the practice of offering people the right to freely distribute copies and modified versions of a work, with the stipulation that the same rights be preserved in derivative works down the line. 

The best known examples of "strong copyleft" licenses are: 

* GNU General Public Licenses ([GPL-2.0](https://spdx.org/licenses/GPL-2.0.html) and [GPL-3.0](https://spdx.org/licenses/GPL-3.0.html)) 
* Affero General Public License ([AGPL-3.0](https://spdx.org/licenses/AGPL-3.0.html))

These licenses follow the free software definition, which gives each person possessing a copy of the work the same freedoms as the author, namely: the freedom to use the work, the freedom to study the work, the freedom to copy and share the work with others, the freedom to modify the work, and the freedom to distribute modified and therefore derivative works. Those derivative works, including forks, would need to retain the same license as the original code if you are not the copyright holder of the original code.

We are using the [SPDX license identifiers](https://spdx.org/licenses/) for the licenses listed above. We will talk more about these later in this course. As an aside, note that for the GNU family of licenses (LGPL, GPL and AGPL), the FSF recommends using identifiers ending with "-only" or "-or-later", as explained in more detail in the following article: ["For Clarity's Sake, Please Don't Say “Licensed under GNU GPL 2”!"](https://www.gnu.org/licenses/identify-licenses-clearly.html) by Richard Stallman.

### Patents

**Patents** have existed in various forms since the Middle Ages. They are a mechanism for protecting intellectual property.

According to [Wikipedia](https://en.wikipedia.org/wiki/United_States_patent_law), the term patent usually refers to the right granted to anyone who invents any new, useful, and non-obvious process, machine, article of manufacture, or composition of matter. Patents provide the right to exclude others from making, using, selling, offering for sale, or importing the patented [invention](https://en.wikipedia.org/wiki/Invention) for the [term of the patent](https://en.wikipedia.org/wiki/Term_of_patent).

By explicitly granting patent rights as part of a license, the license makes clear that others are not excluded from using any of the contributor’s inventions practiced by the code they contribute. Some licenses are considered to have an implicit patent grant, even though no grant is made explicitly in the text.

Software can implement patented inventions. For example, certain software inventions have been patented, and, if you want to use them, you may owe the company that patented them a fee to do so. As a protection, some licenses have made it explicit that those using the code under some specific licenses are granted the right to use any of the patents the contributors have on methods they have included in the code, with no additional charge.

![US Patent Cover](img/us-patent-cover.jpg)

US Patent Cover, by United States Patent and Trademark Office. Source: [Wikipedia](https://en.wikipedia.org/wiki/United_States_patent_law), provided under [CC0-1.0](https://creativecommons.org/publicdomain/zero/1.0/).

### Express Patent Grant with License?

Does the license explicitly refer to patents in its license grant?

| Explicitly excludes patent license | Implicit patent license and/or patents not explicitly mentioned | Explicitly includes patent license |
| :--- | :--- | :--- |
| <ul><li><a href="https://spdx.org/licenses/CC0-1.0.html">CC0-1.0</a></li><li>Other Creative Commons licenses, e.g. <a href="https://spdx.org/licenses/CC-BY-4.0.html">CC-BY-4.0</a></li><li><a href="https://spdx.org/licenses/BSD-3-Clause-Clear.html">BSD-3-Clause-Clear</a></li></ul> | <ul><li><a href="https://spdx.org/licenses/BSD-2-Clause.html">BSD-2-Clause</a> and <a href="https://spdx.org/licenses/BSD-3-Clause.html">BSD-3-Clause</a></li><li><a href="https://spdx.org/licenses/MIT.html">MIT</a></li><li><a href="https://spdx.org/licenses/ISC.html">ISC</a></li><li><a href="https://spdx.org/licenses/Apache-1.0.html">Apache-1.0</a> and <a href="https://spdx.org/licenses/Apache-1.1.html">Apache-1.1</a></li><li><a href="https://spdx.org/licenses/GPL-2.0-only.html">GPL-2.0</a> and <a href="https://spdx.org/licenses/LGPL-2.1-only.html">LGPL-2.1</a></li></ul> | <ul><li><a href="https://spdx.org/licenses/Apache-2.0.html">Apache-2.0</a></li><li><a href="https://spdx.org/licenses/GPL-3.0-only.html">GPL-3.0</a> and <a href="https://spdx.org/licenses/LGPL-3.0-only.html">LGPL-3.0</a></li><li><a href="https://spdx.org/licenses/MPL-1.0.html">MPL-1.0</a>, <a href="https://spdx.org/licenses/MPL-1.1.html">MPL-1.1</a> and <a href="https://spdx.org/licenses/MPL-2.0.html">MPL-2.0</a></li><li><a href="https://spdx.org/licenses/EPL-1.0.html">EPL-1.0</a> and <a href="https://spdx.org/licenses/EPL-2.0.html">EPL-2.0</a></li><li><a href="https://spdx.org/licenses/CDDL-1.0.html">CDDL-1.0</a> and <a href="https://spdx.org/licenses/CDDL-1.1.html">CDDL-1.1</a></li></ul> |

**Note**: Sometimes, projects will use a license that does not explicitly reference patents, but then add a grant of patents in a separate file. An example of this can be seen in the `LICENSE` file (BSD-3-Clause) and the additional `PATENTS` file in the [Golang repo](https://github.com/golang/go/) on GitHub.

If there is not an explicit reference to patents in the license, there may be an implicit grant provided by the terms of the license, but that is an advanced topic that will not be discussed further in this course. Some licenses also explicitly exclude a patent license grant.

If you want to see the text of the licenses and look for the patent grant clauses, just click on the license names and scan to find the references.

### Which License to Choose?

![Licence choose](img/license-choose.png)

When contributing to an existing project, unless the project uses a contribution mechanism with a different inbound license, the common practice is to make your contributions under the terms of the license the project as a whole is governed by. We will talk later in this course about various contribution mechanisms, such as the Developer Certificate of Origin (DCO) and Contributor License Agreements (CLAs), that a project might use for receiving code contributions.

When contributing to or creating a new project, it is very important to clarify the things that someone using the code is required to do (must), what they are permitted to do (can), and what they are forbidden to do (cannot). The license selected is your way of specifying this information. By choosing a standard and commonly-used open source license, you help to make it easier for everyone else to understand what their rights and obligations are.

Some of the properties you may want to consider when choosing a license can be found on the next page.

### Properties to Consider

When choosing a license, it is important to be clear on your goals for releasing the code. Who (what types of people/organizations) do you want to adopt it? Do you want to see any changes people make to your code when they redistribute it? Do you want other people to be able to sell your code for a profit?

You should also consider the following common properties:

* Publish license, copyright notices, change summaries?
* Disclose source?  
* Distribution of modified work?
* Sublicensing?   
* Private or commercial use?
* Patent grant?  
* Able to use trademarks?
* Can code be warrantied?
* Able to hold liable for damages?
* Scope of license: work as a whole or only specific file?

The list on the page contains some common questions you should understand the answer to before making your code public, and choose a license that reflects your answers. This is sometimes a scary task, but in the last couple of years, we’ve seen websites created to help with this, which are listed on the next screen.

### Is There Help Available?

This page lists a few popular sites that discuss the types of licenses and properties to consider in selecting a license for your code, or other creative works. Their purpose is to help you choose a license, and explain more of the background behind some of the options.

#### Source Code

[Open Source Licenses by Category](https://opensource.org/licenses/category) from the Open Source Initiative lists the approved open source licenses.

[Choose an Open Source License](https://choosealicense.com/) is sponsored by GitHub. It walks you through the properties you must consider, helping you decide what license makes sense.

License text sometimes gets treated as "too long, didn’t read" - denoted TL;DR. [tl;drLegal](https://tldrlegal.com/licenses/browse) is trying to clarify the legal text into standard properties. The website creators work with volunteer lawyers to classify and color code the properties associated with specific licenses to help you navigate easier and better understand the existing licenses.

* Blue - Rules you must follow.
* Green - Rules you can follow.
* Red - Things you cannot do.

This is a very useful tool for understanding the terms of some of the common licenses. For example, for Mozilla Public License version 1.0, you cannot hold the contributors liable, but if you use it, you must include copyright, license, state any changes, and disclose the source.

[Various Licenses and Comments About Them](https://www.gnu.org/licenses/license-list.en.html) from the Free Software Foundation's Licensing and Compliance Lab provides a description of many licenses and comments about them.

#### Other Creative Work

[Creative Commons Licenses](https://creativecommons.org/choose/) help you understand license options for images and documentation. An example of this is the [CC-BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/legalcode) license, which this course is licensed under. We encourage you to click the link to the creative commons site, and read the legal code file. It specifies the attribution, share-alike, and other properties associated with the license for this course.

### Additional Resources

In addition, you can take a look at the recently-released resource: [Open Source License Compliance Handbook](https://github.com/finos-osr/OSLC-handbook) from Jilayne Lovejoy and FINOS. The handbook provides "self-serve" information to help users and redistributors of open source software understand the specific requirements for complying with various licenses.

The [SPDX License List](https://spdx.org/licenses/) is another useful resource for identifying licenses. It provides a curated catalog of commonly-seen licenses used in publicly-distributed software. Not all of the licenses are necessarily open source; the License List indicates which ones have been approved by the Open Source Initiative and which have been listed as free/libre by the Free Software Foundation.

The License List does not include interpretations of licenses. Rather, it can be useful when searching for the license text that corresponds to a particular license name or identifier. The License List contributors also maintain versions of the license texts with markup for certain sections of the license text that are considered replaceable while still being substantially the same license, which can be useful when automating detection of license notices in source code.

If you are looking for guidelines on how to structure the license information into your project, we recommend you consult the [REUSE Software](https://reuse.software/) guidelines from the Free Software Foundation Europe. They provide detailed examples on how to add identifiers, and the full text of licenses into projects, as well as scripts to check for compliance with the guidelines.

If you’re trying to use a license that is not on the SPDX License List, they also have good recommendations on how it should be documented so that tools can find the information.

### Mix and Match License?

When can you combine licenses in a project? There is not a single global answer to this question. Interpretations of license compatibility, and which licenses are acceptable for inclusion, depend on the project and distribution the project ships in. Not all projects treat combinations of licenses the same way.

This page provides links to the guidance created by some of the common projects. There are many more projects and distributions than have been listed here, and if you want to include a project in your distribution, it is a good idea to research its licensing policies before trying to contribute.

* [GNU](https://www.gnu.org/licenses/license-list.html)/[Free Software Foundation](https://www.fsf.org/)
* [Fedora Project](https://fedoraproject.org/wiki/Licensing:Main?rd=Licensing#SoftwareLicenses)
* [Debian](https://wiki.debian.org/DFSGLicenses)
* [Android Open Source Project](https://source.android.com/setup/start/licenses)
* [The Apache Software Foundation](https://www.apache.org/legal/resolved.html)

If you do feel the need to contribute code under a different license than the one a project is using, please consult with your legal counsel. License compatibility has a lot of subtleties, and care is needed.

**REMEMBER: You should always check with your legal counsel before contributing to a project on behalf of your employer.**

### What Does a Reference to a License Look Like in a File?

Full license text is frequently long and complex, and not always suitable to put in each file in a project.

It is a common practice to put a `LICENSE` file at the top level of the project and include the full text of the license(s) that may be in effect for the project as a whole. For the other files in a project, by referring to the actual license within each file — even if that reference doesn’t include the full license text — ambiguity is removed as to which license governs that file, particularly when there are multiple licenses being used by a project.

For example, a project may decide to include code from a different project to add new functionality, and the included project is under a different license.

What should a license reference actually look like in a file? You may want to include the following items as a comment in the file with the code:

* A *standard* header for the license (if it exists).
* An *unambiguous* reference to the license intended.

### Making License References Unambiguous

There are several ways to refer to a license in a file in a precise fashion. If there is a standard license header, you can use it. Generally, this is called out as part of the license itself, and is typically several lines of text and contains the formal license name.

Over the last 10 years, the Software Package Data Exchange legal group, or SPDX, has been working to standardize a list of commonly referred to licenses by short identifiers. By using these SPDX license identifiers from the [SPDX License List](https://spdx.org/licenses/), which was described earlier, you can denote the applicable license in a concise, single line reference. You can see examples of these identifiers on the next screen.

You can also use a URL to point to the site where the license has been originally defined. Be careful using only URLs though, as websites "evolve" over time, and may change the location of where they put the license text. For example, a link to GPL-2.0 on the FSF website became a link to GPL-3.0 the day GPL-3.0 was released. Many projects that only had links to the FSF site to indicate their license choice found that the license of their projects on that date was now ambiguous, whether it was intended to be GPL-2.0 or GPL-3.0.

Also, there are some organizations that have teams that review licenses, like OSI and SPDX. By using a URL to refer to the license on one of those sites, you can provide a pointer to the license in effect for the file. These sites have standardized on web locations to put the licenses, so they are less prone to change.

### Examples

#### Identify "GPL-2.0-only"

One very popular license you might encounter is the GNU General Public License version 2, GPL v2 or GPL-2.0 for short. It is used in popular programs like the Linux kernel, for example.

To refer to the license in an unambiguous fashion, at the top of a file, you can put the standard license header. As you can see, while much shorter than the license itself, it does require multiple lines. The FSF recommends that you use this as their preferred format for GPL licensed code.

Standard header: 

```plaintext
/#
# This program is free software; you can redistribute it and/or  
# modify it under the terms of the GNU General Public License
# as published by the Free Software Foundation; version 2.
#
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
# GNU General Public License for more details.
#
# You should have received a copy of the GNU General Public License
# along with this program; if not, write to the Free Software
# Foundation, Inc., 51 Franklin Street, Fifth Floor, Boston, MA 02110-1301, USA.
#/
```

For a reference to a GPL license to be unambiguous, it is important that there is either a version or date specified. For the GPL family of licenses, it is also important to specify whether it is intended to be this version "only" (as in the example shown here), or this version "or any later version".

An additional and more concise format to use is the keyword phrase "SPDX-License-Identifier:", followed by a standardized identifier, like "GPL-2.0-only" which is defined on the SPDX License List. This way, a single line can be included at the top of a file to create an accurate and unambiguous reference to the license in effect.

SPDX-License-Identifier statement:

```plaintext
/#
# SPDX-License-Identifier: GPL-2.0-only
#/
```

URL to the license definition page:

```plaintext
/#   
#  http://www.gnu.org/licenses/old-licenses/gpl-2.0.en.html
#/
```

URL to neutral/refereed site with curated list of licenses (like OSI or SPDX):

```plaintext
/# 
# http://opensource.org/licenses/GPL-2.0
#/
```

#### Identify "Apache-2.0"

Another popular license is Apache 2.0.

In this example, there is a standard header (which actually includes the link to the website with the license text).

Standard header:

```plaintext
/*
* Licensed under the Apache License, Version 2.0 (the "License");
* you may not use this file except in compliance with the License.
* You may obtain a copy of the License at
*
*    http://www.apache.org/licenses/LICENSE-2.0
*
* Unless required by applicable law or agreed to in writing, software
* distributed under the License is distributed on an "AS IS" BASIS,
* WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
* See the License for the specific language governing permissions and
* limitations under the License.
*/
```

In a similar fashion, the use of an SPDX License Identifier is also helpful.

SPDX-License-Identifier statement:

```plaintext
/*
* SPDX-License-Identifier: Apache-2.0
*/
```

URL to the license definition page:

```plaintext
/*
* http://www.apache.org/licenses/LICENSE-2.0
*/
```

URL to neutral/refereed site with curated list of licenses (like OSI or SPDX):

```plaintext
/*      
* http://opensource.org/licenses/Apache-2.0
*/
```

#### Identify "CC-BY-SA-4.0"

Another example that you might encounter is the use of the Creative Commons licenses. These licenses are typically intended for artistic work and documentation, rather than software.

There is a standard header for the licenses in this family, as well as a graphic. The Creative Commons website has a way of creating this graphic embedded with specific information about the work under the license. CC-BY-SA-4.0 is the license that this course is being released under.

Standard header:

![Creative Commons Attribution-ShareAlike icon](img/cc-by-sa-icon.png)

```plaintext
This work is licensed under a Creative Commons Attribution-ShareAlike 4.0 International License.
```

In a similar fashion to the other examples, an SPDX short form license identifier can be used to specify the license.

SPDX-License-Identifier statement:

```plaintext
/*
* SPDX-License-Identifier: CC-BY-SA-4.0
*/
```

URL to the license definition page:

```plaintext
/*      
* http://creativecommons.org/licenses/by-sa/4.0/legalcode
*/
```

URL to neutral/refereed site with curated list of licenses (like OSI or SPDX):

```plaintext
/*      
* http://spdx.org/licenses/CC-BY-SA-4.0.html
*/
```

#### Identify multiple licenses in one file

User's choice of either license:

```plaintext
/*
* SPDX-License-Identifier: Apache-2.0 OR LGPL-3.0-only
*/
```

User must comply with both licenses:

```plaintext
/*
* SPDX-License-Identifier: Apache-2.0 AND LGPL-3.0-only
*/
```

Sometimes a project or file might be distributed under a choice of two or more licenses. This might be because the licensor wants to enable broader compatibility and reuse of their code. In the first case shown above, the recipient can choose to use it under either version 2 of the Apache license or under version 3 of the LGPL.

By contrast, sometimes a project or file might require the recipient to comply with both licenses in order to use or redistribute it. This might be because it contains content originating from two different projects that were under different licenses. Even if the licenses are compatible, the recipient may need to comply with both of their requirements. In the second case shown above, the recipient would need to comply with both licenses.

Note that just saying that a project is "dual-licensed" could be seen as ambiguous, about whether the licensor intends it to be "either/or" or "both/and". Using clear language about the intended outbound license makes it easier for the community to understand and fulfill their responsibilities. One unambiguous way to do this is to use SPDX license expressions with "OR" or "AND", as shown in the examples above. More information about SPDX short-form license identifiers can be found on [the SPDX website](https://spdx.org/ids-how).

## Summary

### Conclusion

You should now be able to discuss the types of licenses typically used in software source code. You should also know where to find more information about the most common open source licenses, and how to refer to them in software source code.
