# Course Introduction

## Course Information

### Course Introduction

**Welcome to the Open Source Licensing Basics for Software Developers (LFC191) course!**

Understanding how copyright and licenses work, and being able to clearly and accurately specify them, is key to ensuring that your contributions are acceptable for open source projects to use, and that licensing statements reflect your intentions correctly.

Licenses give those who want to use your code permission in advance. The actual permissions granted are spelled out in the selection of a license that the copyright holder chooses.

This course is designed to help software developers, and those involved in producing software that will be used or distributed, to understand why it is important to add information about licenses and copyrights to their code, as well as how to do so.

It also provides information on how to create file notices with copyright and license statements. Being able to minimize problems and ambiguity is useful for internal corporate projects, as well as for contributing to open source projects.

An overview of the types of licenses to consider, as well as the mechanisms for contributing code, is also summarized.

### Course Learning Objectives

By the end of this course, you should be able to:

* Understand why it is important to add copyright and licenses to code.
* Know how to do so efficiently.
* Understand the mechanisms used when contributing code to a project.

### Meet Your Instructors

#### Kate Stewart

![Kate Stewart](img/kate-stewart.jpg)

Kate Stewart is a Senior Director of Strategic Programs, responsible for the Open Compliance program encompassing the SPDX, FOSSology, OpenChain, and other compliance related projects. Kate was one of the founders of SPDX in 2010, and is currently the specification lead. Since joining the Linux Foundation, she has also launched Real-Time Linux, Zephyr, CHAOSS, ELISA and ACT Projects.

With over 30 years of experience in the software industry, she has held a variety of roles and worked as a developer in Canada, Australia, and the US and for the last 20 years has managed software development teams in the US, Canada, UK, India, and China. She received her Master’s in computer science from University of Waterloo and Bachelor’s of computer science (co-op program) from the University of Manitoba.

#### Steve Winslow

![Steve Winslow](img/steve-winslow.jpg)

Steve Winslow is Director of Strategic Programs at the Linux Foundation. He runs the Linux Foundation’s license scanning and analysis support program, advising open source projects about licenses identified in their source code and dependencies. Steve is the co-lead of the SPDX legal team, and is also involved with projects such as FOSSology and the Community Data License Agreement; manages the Linux Foundation’s trademark program; and assists on other legal, policy and governance matters for projects.

### Course Audience and Requirements

This course is designed to help software developers and those involved in producing software that will be distributed, as well as anyone interested in contributing to open source projects.

No previous experience is required.

### Why Bother with Licenses and Copyright in Code?

![XKCD: Copyright](img/xkcd-14.jpg)

Retrieved from [xkcd.com](https://xkcd.com/14/), provided under [CC-BY-NC-2.5](https://creativecommons.org/licenses/by-nc/2.5/).

A **license** lets people know how code can be used, and how it can be combined with other software.

The image above is an early xkcd image. Because the creator had specified a license for it, after reading the terms, we know we can include it in this course while respecting the rights of the creator.

As this course is freely available with the purpose of education, and because attribution has been provided, it abides by the terms of the CC-BY-NC 2.5 license. The purpose of this course is not for monetary compensation or commercial purposes, it is for education, so we can include this image to illustrate the point.

The purpose of stating a license is to give people who want to use your work, permission in advance.

Much of the technology infrastructure we take for granted today is due to the licensing decisions specific copyright holders made. So, if you want to use someone’s work, please respect the license they choose to make it available under.

Many software and hardware developers will encounter open source materials on the job or in personal projects.

Open source materials can include things like software, hardware designs, tools, documents, audio recordings, and image files.

Although open source materials are usually freely available, they are typically provided under a stated license. The license chosen is what permits project material to be considered as "open source", and the **copyright holder** for the material is the decider of the license.

Copyright is established by national laws, and gives the copyright holder some exclusive rights to control a creative work’s use and distribution.

Copyright holders have exclusive rights to their creative expression. Copyright is used to protect tangible forms of expression, which are sometimes referred to as original works of authorship.

Normally, we think of copyrights protecting things like books, movies, music, maps, and art. Copyright can also be used to protect the expression of hardware designs and software, as well as other creative works.

The rights relevant to source code may vary from country to country, but can be generally understood as the exclusive right to: copy, modify or create derivative works, and distribute. Other rights include activities such as performing a play or public display of a painting. We will talk more about this shortly.

## Before You Begin

### Course Timing

This course is entirely self-paced; there is no fixed schedule for going through the material. You can go through the course at your own pace, and you will always be returned to exactly where you left off when you come back to start a new session. However, we still suggest you avoid long breaks in between periods of work, as learning will be faster and content retention improved.

The chapters in the course have been designed to build on one another. It is probably best to work through them in sequence; if you skip or only skim some chapters quickly, you may find there are topics being discussed you have not been exposed to yet. But this is all self-paced, and you can always go back, so you can thread your own path through the material.

### Assessments

At the end of each chapter, you will find a series of **ungraded knowledge check questions**. These questions were designed with one goal in mind: to help you better comprehend the course content and reinforce what you have learned. 

To complete this course, **you will be required to take a final exam**. You must score **90% or better** to pass the exam and complete the course. If you fail the exam, you will have the opportunity to retake it as many times as needed, until you obtain a passing grade.

### Legal Disclaimer, Course Copyright and License

Copyright 2016-2021, The Linux Foundation.

This course is licensed under a [Creative Commons Attribution-ShareAlike 4.0 International License (CC-BY-SA-4.0)](https://creativecommons.org/licenses/by-sa/4.0/), except for content from other sources where a different license is otherwise noted.

---

**The following are some recommended best practices, but you should always consult with your own legal counsel.**

This course does NOT constitute legal advice. Legal advice is always very fact specific and specific to the laws of the applicable jurisdiction.

Always consult with your own legal counsel and follow the counsel’s advice if it differs from the recommendations provided in this course.

This course has been created by Linux Foundation employees, so the Linux Foundation is considered the copyright holder and able to determine the license.

This course is licensed under the CC-BY-SA-4.0 license. This is one of several licenses developed by the Creative Commons organization. This specific license lets others remix, tweak, and build upon this work, even for commercial purposes, as long as they credit this work and license their new creations under identical terms.

CC-BY-SA-4.0 is similar to the license used by Wikipedia, and is recommended for materials that would benefit from incorporating content from Wikipedia and similarly licensed projects. We will talk more about this later in the course.

## The Linux Foundation

### The Linux Foundation

![The Linux Foundation logo](img/linux-foundation-logo.jpg)

[The Linux Foundation](https://www.linuxfoundation.org/) provides a neutral, trusted hub for developers to code, manage, and scale open technology projects. Founded in 2000, The Linux Foundation is supported by more than 1,000 members and is the world’s leading home for collaboration on open source software, open standards, open data and open hardware. The Linux Foundation’s methodology focuses on leveraging best practices and addressing the needs of contributors, users and solution providers to create sustainable models for open collaboration.

The Linux Foundation hosts Linux, the world's largest and most pervasive open source software project in history. It is also home to Linux creator Linus Torvalds and lead maintainer Greg Kroah-Hartman. The success of Linux has catalyzed growth in the open source community, demonstrating the commercial efficacy of open source and inspiring countless new projects across all industries and levels of the technology stack.

As a result, the Linux Foundation today hosts far more than Linux; it is the umbrella for many critical open source projects that power corporations today, spanning virtually all industry sectors. Some of the technologies we focus on include big data and analytics, networking, embedded systems and IoT, web tools, cloud computing, edge computing, automotive, security, blockchain, and many more.

### The Linux Foundation Events

Over 85,000 open source technologists and leaders worldwide gather at Linux Foundation events annually to share ideas, learn and collaborate. Linux Foundation events are the meeting place of choice for open source maintainers, developers, architects, infrastructure managers, and sysadmins and technologists leading open source program offices, and other critical leadership functions.

These events are the best place to gain visibility within the open source community quickly and advance open source development work by forming connections with the people evaluating and creating the next generation of technology. They provide a forum to share and gain knowledge, help organizations identify software trends early to inform future technology investments, connect employers with talent, and showcase technologies and services to influential open source professionals, media, and analysts around the globe.

The Linux Foundation hosts an increasing number of events each year, including:

* Open Source Summit North America, Europe, and Japan
* Embedded Linux Conference North America and Europe
* Open Networking & Edge Summit
* KubeCon + CloudNativeCon North America, Europe, and China
* Automotive Linux Summit
* KVM Forum
* Linux Storage Filesystem and Memory Management Summit
* Linux Security Summit North America and Europe
* Linux Kernel Maintainer Summit
* The Linux Foundation Member Summit
* Open Compliance Summit
* And many more.

You can learn more about the [Linux Foundation events](https://events.linuxfoundation.org/) online.

### Training Venues

The Linux Foundation's training is for the community, by the community, and features instructors and content straight from the leaders of the Linux developer community.

The Linux Foundation offers several types of training:

* Classroom
* Online
* On-site
* Events-based.

Attendees receive Linux and open source software training that is distribution-flexible, technically advanced and created with the actual leaders of the Linux and open source software development community themselves. The Linux Foundation courses give attendees the broad, foundational knowledge and networking needed to thrive in their careers today. With either online or in-person training, The Linux Foundation classes can keep you or your developers ahead of the curve on open source essentials.

### The Linux Foundation Training Offerings

![The Linux Foundation Training and Certification logo](img/linux-foundation-training.png)

Our current course offerings include:

* Linux Programming & Development Training
* Enterprise IT & Linux System Administration Courses
* Open Source Compliance Courses.

To get more information about specific courses offered by the Linux Foundation, including technical requirements and other logistics, visit the [Linux Foundation training](https://training.linuxfoundation.org/) website.

### The Linux Foundation Certifications

The [Linux Foundation certifications](https://training.linuxfoundation.org/certification/) give you a way to differentiate yourself in a job market that's hungry for your skills. We've taken a new, innovative approach to open source certification that allows you to showcase your skills in a way that other peers will respect and employers will trust:

You can take your certification exam from any computer, anywhere, at any time:

* The certification exams are performance-based​
* The exams are distribution-flexible
* The exams are up-to-date, testing knowledge and skills that actually matter in today's IT environment.

### Training/Certification Firewall

The Linux Foundation has two separate training divisions: Course Delivery and Certification. These two divisions are separated by a **firewall**. 

The curriculum development and maintenance division of the Linux Foundation Training department has no direct role in developing, administering, or grading certification exams. 

Enforcing this self-imposed firewall ensures that independent organizations and companies can develop third party training material, geared towards helping test takers pass their certification exams. 

Furthermore, it ensures that there are no secret "tips" (or secrets in general) that one needs to be familiar with in order to succeed. 

It also permits the Linux Foundation to develop a very robust set of courses that do far more than teach the test, but rather equip attendees with a broad knowledge of the many areas they may be required to master to have a successful career in open source system administration.
