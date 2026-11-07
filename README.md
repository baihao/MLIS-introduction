LaTeX Template for Presentations
================================

This is the presentation template of the chair Software Design and
Quality (SDQ) at the Institute for Program Structures and Data Organization (IPD)
of the Karlsruhe Institute of Technology (KIT).

Author: Dr.-Ing. Erik Burger (burger@kit.edu)
with contributions by Christian Hammer, Klaus Krogmann and Maximilian Schambach

See https://sdqweb.ipd.kit.edu/wiki/Dokumentvorlagen

Feedback and Suggestions
========================

Please use the issue tracker at https://git.scc.kit.edu/i43/dokumentvorlagen/praesentationen/beamer/-/issues to report problems with the template or to request extensions. You are also welcome to propose a change via merge request.

Usage
=====

This package is a template for presentations in the KIT design (https://intranet.kit.edu/gestaltungsrichtlinien.php, version of 1 August 2020).

It is based on LaTeX Beamer (https://ctan.org/pkg/beamer).

Options of the document class `sdqbeamer`
-----------------------------------------
The following options set the aspect ratio of the slides:

| Aspect ratio     | Option              |
| ---------------- | ------------------- |
| 16:9             | `16:9`  (default)   |
| 16:10            | `16:10`             |
| 4:3              | `4:3`               |

By default, the footer font size is larger than specified in the design guidelines. The official size (font size 9 -> 6) can be enforced with the option `smallfoot`.

| Footer font size      | Option               |
| ----------------------| -------------------- |
| slightly larger (12pt)| `bigfoot` (default)  |
| KIT standard (9pt)    | `smallfoot`          |

The position of the navigation bar can be set with the following options:

| Position                 | Option           | Remark                                     |
| ------------------------ | ---------------- | ------------------------------------------ |
| above the separation line| `navbarinline`   | default                                    |
| below the separation line| `navbarinfooter` | no subsection dots, size `smallfoot`       |
| sidebar on the left      | `navbarside`     | no subsection dots                         |
| no navigation bar        | `navbaroff`      |                                            |
| KIT standard             | `navbarkit`      | equivalent to `navbaroff` and `smallfoot`  |

German and English are available as languages. The language choice automatically selects the matching logos and formats (e.g. date).

| Language |                 |
| -------- |---------------- |
| German   | `de` (default)  |
| English  | `en`            |

Example: `\documentclass[de,16:9,navbarinline]{sdqbeamer}`

Title image
-----------

The image on the title slide can be set with the command

`\titleimage{myimage}` (without file extension)

To use your own image, place the file (e.g. `myimage.jpg`) in the `logos/` directory and adjust the command. A generic image from the KIT image library (https://intranet.kit.edu/gestaltungsrichtlinien.php) is included in the file `logos/banner_2020_kit.jpg`. If no title image should be inserted, set `\titleimage{}`.

For 16:9 slides the image ratio should be 160:37, for 4:3 slides 63:20. Wider images can also be used, since the title image is scaled to the height of the frame and centred.

Logo and name of department/KIT faculty/institute
-------------------------------------------------

The logo at the top right of the title slide can be set with the following command:

`\grouplogo{mylogo}` (without file extension)

To use your own logo, place the file (e.g. `mylogo.pdf`) in the `logos/` directory and adjust the command. If no logo should be inserted, set `\grouplogo{}`.

The group name can be set with the following command:

`\groupname{Software Design and Quality}`.

The group name appears at the bottom right of the footer. Long names are wrapped onto two lines. If the group name is left empty (`\groupname{}`), the full width of the footer is used for the author names and title.

LaTeX in general
----------------
See https://sdqweb.ipd.kit.edu/wiki/LaTeX

File structure
==============
`presentation.tex`
------------------
Main file of the LaTeX document.

`presentation.bib`
------------------
Example file for BibTeX references
https://sdqweb.ipd.kit.edu/wiki/BibTeX-Literaturlisten

`sdqbeamer.cls`
-----------------
Document class for presentations in the KIT design.

`logos/`
--------
This directory contains the KIT logo as PDF and the background image of the title slide as JPG.

`CHANGELOG.md`
--------------
Documentation of the changes in each version.

`README.md`
-----------
This text.