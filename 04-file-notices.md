# File notices

## Introduction

### Section Overview

A file notice is the information included in a software source file, indicating the copyright notice and the license.

The form of the copyright notice was summarized in Section 3. The form of the license reference was summarized in Section 2. Together the copyright notice and the license reference form a file notice.

### Learning Objectives

By the end of this section, you should be able to:

* Explain what is needed to form a typical file notice.
* Recognize some specific common examples that illustrate valid file notices.

## File Notices

### What Are Valid File Notices?

What are valid file notices? Valid file notices have the following characteristics: they define in a clear manner the license that the file is governed by, and may include information or references to copyright holders. A file notice may also provide additional information about authorship, when the author is not the copyright holder.

If a file notice contains this information using an unambiguous license reference, then this key information can be machine detectable.

Enabling licensing information to be machine detectable greatly improves the handling of compliance information. It also makes it easier for those using open source software to understand the terms of using it, and to know who to ask questions of when something is ambiguous.

By convention, file notices are usually placed at the start of the file.

### Example: Linux

![Linux](img/linux.jpg)

```plaintext
// SPDX-License-Identifier: GPL-2.0-only
/*
 *  ARM64 Specific Low-Level ACPI Boot Support
 *
 *  Copyright (C) 2013-2014, Linaro Ltd.
 *      Author: Al Stone <al.stone@linaro.org>
 *      Author: Graeme Gregory <graeme.gregory@linaro.org>
 *      Author: Hanjun Guo <hanjun.guo@linaro.org>
 *      Author: Tomasz Nowicki <tomasz.nowicki@linaro.org>
 *      Author: Naresh Bhat <naresh.bhat@linaro.org>
 */
 ```

The first [example](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/tree/arch/arm64/kernel/acpi.c) we will look at is from the Linux operating system. In this file, `acpi.c,` the named copyright holder is Linaro. The use of "Copyright" and the copyright symbol is redundant, but not a major issue. The work was originally published in 2013, and there were significant updates to it in 2014. This is indicated by the use of a date range. The copyright statement consists of that single line.

As a nicety (but not an official part of the copyright statement), there are five authors who have contributed to this file that are willing to be contacted if there are questions. This is indicated by the listing of their full name and email addresses. The authors in this case are not the copyright holders, as the work was done for hire as part of their employment with Linaro, which is why Linaro is indicated as the copyright holder.

The license here is the GPL version 2. This is indicated by the use of an SPDX short-form identifier in the first line of the file.

As a point of interest, if you look at the [git log history for this file](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/log/arch/arm64/kernel/acpi.c), you can see that many changes have been made to this file since 2014. Some of these changes were minor tweaks or even deletions without adding content, but some were of significant length (with a few >100 lines of code). If those subsequent additions contained copyrightable content, then the "2013-2014" year range in the copyright notice may be incomplete. Also, if any of the subsequent contributors were not employed by Linaro, then the copyright notice may not accurately list all copyright holders. This reflects how reliance solely on the copyright notice may be misleading or insufficient, if you are looking to understand the full copyright ownership context for a file or project.

### Example: FOSSology

![FOSSology](img/fossology.png)

```plaintext
/**************************************************************
 Copyright (C) 2006-2013 Hewlett-Packard Development Company, L.P.

 This program is free software; you can redistribute it and/or
 modify it under the terms of the GNU General Public License
 version 2 as published by the Free Software Foundation.

 This program is distributed in the hope that it will be useful,
 but WITHOUT ANY WARRANTY; without even the implied warranty of
 MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
 GNU General Public License for more details.

 You should have received a copy of the GNU General Public License along
 with this program; if not, write to the Free Software Foundation, Inc.,
 51 Franklin Street, Fifth Floor, Boston, MA 02110-1301, USA.

 ***************************************************************/
```

In another [example](https://github.com/fossology/fossology/blob/master/src/nomos/agent/list.c), this one from FOSSology, the standard header indicating the license as GPL version 2 is placed after the copyright statements.

In this file, the full official text from the standard license header was used. The SPDX identifier was used in the other example, but in either case, it’s pretty clear that the license the file is governed under is GPL version 2, which is the important thing.

### Example: gcc

![GNU](img/gnu.png)

```plaintext
/* Common hooks for AArch64.
    Copyright (C) 2012-2015 Free Software Foundation, Inc.
    Contributed by ARM Ltd.

    This file is part of GCC.

    GCC is free software; you can redistribute it and/or modify it
    under the terms of the GNU General Public License as published
    by the Free Software Foundation; either version 3, or (at your
    option) any later version.

    GCC is distributed in the hope that it will be useful, but WITHOUT
    ANY WARRANTY; without even the implied warranty of MERCHANTABILITY
    or FITNESS FOR A PARTICULAR PURPOSE.  See the GNU General Public
    License for more details.

    You should have received a copy of the GNU General Public License
    along with GCC; see the file COPYING3.  If not see
    <http://www.gnu.org/licenses/>.  */
```

In this [example](https://github.com/gcc-mirror/gcc/blob/master/gcc/common/config/aarch64/aarch64-common.c), `aarch64-common.c`, the GNU project requires copyright assignment as part of the terms of contribution, so the copyright is assigned to the Free Software Foundation from ARM Ltd. The "Contributed by ARM Ltd." statement is not a copyright statement, but additional information about authorship.

The copyright statement has the redundant use of Copyright and © here, but that is ok.

The first contribution to this file was made in 2012, and significant updates happened in 2013, 2014 and 2015 as the new ARM64 architecture information was contributed. This range of dates is indicated by 2012-2015.

After the copyright, there is the standard license header for the GNU General Public License (which is known as GPL) version 3 or later. The GPL states that if no version number is specified by the licensor, then the licensee can use any version of the GPL that has been published by the Free Software Foundation. For clarity, it is always a good practice to specify the version of the license the code is governed under, so the intent is clear. There are significant differences in terms between GPL v2 and GPL v3 and code that is specifically limited to GPL-2.0-only cannot be combined with code that is licensed under GPL-3.0.

### Example: Nova

![OpenStack](img/openstack.png)

```plaintext
# Copyright 2010 United States Government as represented by the
# Administrator of the National Aeronautics and Space Administration.
# Copyright 2011 Justin Santa Barbara
# All Rights Reserved.
#
#    Licensed under the Apache License, Version 2.0 (the "License"); you may
#    not use this file except in compliance with the License. You may obtain
#    a copy of the License at
#
#         http://www.apache.org/licenses/LICENSE-2.0
#
#    Unless required by applicable law or agreed to in writing, software
#    distributed under the License is distributed on an "AS IS" BASIS, WITHOUT
#    WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the
#    License for the specific language governing permissions and limitations
#    under the License.
```

Another common open source family of projects is [OpenStack](https://docs.openstack.org/keystone/10.0.2/10.0.2/_modules/keystone/common/authorization.html). Nova is one of the projects in this family.

This license file for this project was created in 2010, and is copyrighted by the US Government. In 2011, Justin Barbara made significant changes to the project and is asserting copyright as well.

After the copyright notices, the Apache 2.0 License standard header is used to indicate the license the project is governed under. The standard header contains a web URL, where the text of the license can be found, which is included in some standard headers. After the explicit specification of "Licensed under the Apache License, Version 2.0", including the web link is redundant, but it is part of the Apache standard header, so it’s fine.

Generally, redundant information is ok, as long as it is consistent.

A specific and fairly common example of something that is inconsistent is a copyright notice and then an indication that the materials are public domain. Unless it is a US government created work, it is very unlikely to be successfully dedicated to the public domain. A copyright notice without a license statement indicates that there is a copyright holder, but there is no license granted unless otherwise stated in another place that applies to this file.

It is not advised to change the header on someone else’s code, even when there is redundant information. The best policy is to contact the author and ask that person to fix it. Similarly, when there is inconsistent information, contact the author or authors and ask for clarification and update.

### Example: Das U-Boot

```plaintext
/* SPDX-License-Identifier: GPL-2.0+ */
/*
 * (C) Copyright 2002
 * Wolfgang Denk, DENX Software Engineering, wd@denx.de.
 *
 * (C) Copyright 2010
 * Michael Zaidman, Kodak, michael.zaidman@kodak.com
 * post_word_{load|store} cleanup.
 */
```

In recent years, some projects have started to adopt the use of SPDX short form license identifiers, to indicate clearly which license is in effect in a file.

In this [example](https://github.com/u-boot/u-boot/blob/master/include/post.h), the file was created in 2002 by Wolfgang Denk, as part of his work at DENX Software Engineering. It is not clear from this copyright statement whether he owns it as an individual (Wolfgang Denk) or as an organization (DENX Software Engineering), so contacting

Wolfgang might be required to clarify this if he stopped working for DENX Software Engineering in the future. In 2010, Michael Zaidman from Kodak made significant changes and added his copyright. Here, Kodak is likely the copyright holder, but Michael Zaidman may own the copyright too, depending on his employment contract.

After this, you see the SPDX-License-Identifier which is "GPL-2.0+". This is a short form that has been standardized by the SPDX legal group, as a common way to refer to the GPL version 2 or later license. As discussed earlier, in the past couple of years, with input from the Free Software Foundation, the GNU family of licenses have shifted to use either "GPL-2.0-only" or "GPL-2.0-or-later" for their short identifiers, rather than "GPL-2.0+" which is still valid but is deprecated. So the example shown here could be updated to use the new format. The full list of all SPDX short form identifiers can be found on the [SPDX web site](https://spdx.org/licenses/). The full text of the license is available on that site, as well as links to where the original text was copied from.

### Example: Zephyr

```plaintext
/*
 * Copyright (c) 2018 Intel Corporation
 *
 * SPDX-License-Identifier: Apache-2.0
 */
```

In this [example](https://github.com/zephyrproject-rtos/zephyr/blob/master/kernel/sched.c), the file `sched.c` was created in 2018 by someone working for Intel, so the original copyright notice specifies Intel Corporation. Since the file was created, 30 individuals can be seen to have participated in adding content to this file, some who may not be working for Intel.

The license the file is under is the Apache 2 license, which is denoted here by use of an SPDX identifier "Apache-2.0".

## Summary

### Conclusion

This section explained what is needed to form a typical file notice and provided some specific common examples to illustrate valid file notices.
