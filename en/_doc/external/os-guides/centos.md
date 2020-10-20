---
lang: en
layout: doc
permalink: /doc/templates/centos/
ref: 81
title: CentOS Template
---

# CentOS Template

If you would like to use a stable, predictable, manageable and reproducible distribution in your AppVMs, you can install the CentOS template, provided by Qubes in ready to use binary package.

For the minimal version, please see [Minimal TemplateVMs](/doc/templates/minimal/)


## Installation

The standard CentOS TemplateVM can be installed with the following command in dom0, where `X` is the desired version number:

    [user@dom0 ~]$ sudo qubes-dom0-update --enablerepo=qubes-templates-community qubes-template-centos-X

To switch, reinstall and uninstall a CentOS TemplateVM that is already installed in your system, see *How to [switch], [reinstall] and [uninstall]*.

#### After Installing

After a fresh install, we recommend to [Update the TemplateVM](/doc/software-update-vm/).

## Want to contribute?

*   [How can I contribute to the Qubes Project?](/doc/contributing/)

*   [Guidelines for Documentation Contributors](/doc/doc-guidelines/)

[switch]: /doc/templates/#switching
[reinstall]: /doc/reinstall-template/
[uninstall]: /doc/templates/#uninstalling
[Minimal TemplateVMs]: /doc/templates/minimal/
[Xfce TemplateVMs]: /doc/templates/xfce/