# Contributing to projects

## Introduction

### Section Overview

Before contributing code upstream to an open source project, you need to make sure it is ok for you to do so.

If you do not work for a company or organization, and are making the contributions of code or content as an individual where you own the copyright, it tends to be fairly straightforward. Projects have individual contributor guidelines to follow and these should be read carefully, any necessary paperwork filed or sign-offs prepared, and then patches sent to the project.

If you do work for an organization, you will need to check with your management that it is ok to send work you have been doing to the upstream project. The company may need to sign some form of contributor agreement or assign copyrights, or you may need to provide DCO (Developer Certificate of Origin) sign-offs, in order for the contribution to be accepted.

### Learning Objectives

By the end of this section, you should be able to:

* Understand the common terms under which projects accept contributions, and what to check for.

## Contributing to Projects

### Get Approval for Contributing Employer-Owned Code

If you are contributing code on behalf of your employer — in other words, code that is owned by your employer and not by you — then you should make sure your employer will permit you to contribute it to the project.

Part of this may include your employer’s acceptance of the applicable contribution mechanism, such as signing a Contributor License Agreement (CLA) or permitting a Developer Certificate of Origin (DCO) sign-off. These contribution mechanisms are described in more detail on the following pages.

Additionally, another part may involve your employer determining whether the subject matter of your proposed contribution is appropriate to submit to the project. Your employer might be comfortable with contributing code or content for certain functionality, but might object to other types of code being contributed. Every organization may have a different set of policies and procedures for these determinations. You should check with your company’s open source program office, legal team, or other appropriate group before you contribute code that is owned by the company.

### Contribution Mechanisms

To preserve a project’s goals, and to ensure that downstream users can enjoy the rights granted by the project’s license, the project may require some formalities before it can accept changes from you.

Typically there will be some documentation in a `CONTRIBUTING` file in the project repository, or on the project website and pages, describing what formalities are needed.

Not all projects require these formalities. Many projects on GitHub will accept pull requests without anything required other than a code patch. However, many larger and significant open source projects use formal contribution mechanisms to help protect the project community, users and contributors, and their expectations.

Examples of formal contribution mechanisms include:

* Contributor License Agreements (CLAs)
  * e.g. Apache Software Foundation, Google, Kubernetes
* Copyright Assignment
  * e.g. GNU toolchain
* Developer’s Certificate of Origin (DCO)
  * e.g. Linux kernel, Zephyr

### Contributor License Agreements (CLAs)

A Contributor License Agreement (CLA) is an agreement between the project and the owner of the contribution. As its name suggests, the contributor grants a **license** to the project. The CLA’s text describes the scope of the license that is granted.

This means that the owner of the contribution continues to own it. Signing a CLA doesn’t mean that they transfer their ownership to the project. Rather, the CLA grants a license, but the owner of the contribution still owns its copyright, and can use and license it to others in other ways.

Every project’s CLA might be different, and might grant a different scope of license, have different requirements, etc. The scope of licenses being granted to the project are often not the same as the "outbound" license granted by the project to the rest of the world. Because of this, you and/or your legal team will likely want to review closely any CLA before you sign it.

Many projects that use CLAs will have two different forms:

* **Individual** - An Individual CLA (ICLA) is intended for individuals who are contributing code that they own.
* **Corporate** - A Corporate CLA (CCLA) is intended for companies and organizations, where an employee is contributing code on behalf of their employer.

If you are contributing code owned by your employer, you should have your legal team review the Corporate CLA and, if they approve it, have it signed by someone who is authorized by your company to sign contracts like CLAs. You should not bypass your company’s review, approval and signing of a CCLA by instead signing an Individual CLA yourself, if the code is owned by, and being contributed on behalf of, your employer.

### Copyright Assignment

A Copyright Assignment agreement, like a CLA, is also an agreement between the project and the owner of the contribution. However, unlike CLAs, a Copyright Assignment actually transfers (or "assigns") ownership of the copyright from the contributor to the project. The contributor will no longer own the copyright in the contributed code.

Copyright assignment is typically used by projects that want to own the copyrights for enforcement purposes, and to retain the right to relicense a project at some future date. (CLAs may also enable relicensing of a project, depending on the text of the particular CLA.)

A common example where this is used is by the Free Software Foundation, or FSF, for contributions to the GNU compiler. Here they ask for the copyright to be assigned as one contribution mechanism before they accept changes in, so that the project will own all copyrights in the contributions.

In addition to being used as supporting their approach to enforcing the terms of the GPL, the assignment of copyright in this project allowed the FSF as the copyright owner to work with other organizations and individuals to enforce the principles of the license, or to issue materials such as the GCC Runtime Library Exceptions that clarify the license or offer additional permissions that could be considered a change in the license terms.

### The Developer's Certificate of Origin 1.1

Another method that is used by some projects is the Developer’s Certificate of Origin. Instead of using a Contributor License Agreement, in May 2004, the kernel development community decided to standardize on a requirement to adhere to a Developer’s Certificate of Origin (also known as the DCO) for contributions to the Linux kernel.

In the DCO, the contributor indicates at the time they submit a contribution — via a sign-off statement in the metadata provided together with the contribution — that they have the right to submit the change under the indicated license, have it be public, and if it is based on a previous work, that too is ok to submit, to the best of the contributor’s knowledge.

Below you can find the text of the ["Developer's Certificate of Origin Version 1.1"](https://www.developercertificate.org/):

```plaintext
By making a contribution to this project, I certify that:

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
```

In addition, you can also find it in the Linux Kernel Source Tree, [Documentation/process/submitting-patches.rst](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/tree/Documentation/process/submitting-patches.rst) file.

Other open source projects have adopted the use of this method instead of CLAs or assignment agreements. For this mechanism to work, there should be a license in each source file and there is an understanding that what you are submitting is compatible with the open source license indicated in the file you are submitting a change to, and a signed-off notation is used as shown on the next screen.

### How to Sign-Off for the DCO

The DCO does not involve getting a signed agreement (whether from you or your employer). Instead, if you are submitting to a project that uses a DCO, you will be adding a "signed-off" statement in your patch.

A signed-off statement follows the following syntax.

A "Signed-off-by:" tag followed by the person’s name and email address. This statement can easily be added to your commit with a single '-s' command-line flag when using the Git tools.

```plaintext
Signed-off-by: Linus Torvalds <torvalds@linuxfoundation.org>
```

In the example we provide, this is what Linus Torvalds’ signed-off-by statement would look like for a change he wanted to apply to the kernel.

Some tools make it easier to enforce DCO checks, meaning that they help ensure that patches submitted for inclusion are only incorporated into the project code if they were accompanied by a "Signed-off-by:" statement. For example, on GitHub the [DCO app](https://github.com/apps/dco) enables these checks when a pull request is submitted.

## Summary

### Conclusion

You should now have a basic knowledge of the common mechanisms projects use to accept contributions, and what to check for.
