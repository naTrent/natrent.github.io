---
title: "Should I Import or Open project In IntelliJ?"
alt_title: "Should I Import or Open project In IntelliJ?"
---

## TLTR
### Open vs Import Project in IntelliJ

In the context of _Maven_ related project:

**Import** - this option open the folder and looks for a pom.xml file to import the project and all dependencies.
This option has some additional wizard screen to customize the import of the new project.

**Open** - this option at first looks for _.idea_ folder and if it couldn't find one starts looking for a pom.xml file. 
**Open** option doesn't have additional wizard screens to customize the imported project.

## Open vs Import Project in IntelliJ with Git version control

In my case I have a problem with Open option because I removed from my repo _.idea_ folder manually and IntelliJ somehow doesn't see that.
Of course I removed cache folder for the project and even for IDE itself but it din't help. When I try to rerun maven dependencies IDE did nothing.
It seamed that IntelliJ has already seen them as imported.

## Solution

What helped me is that:
    1. After removed _.idea_ folder manually form repository, check if in _.gitignore_ file you have added _.idea_ entry in the file.
    2. Clear all project related cache in IDE file structure.
    3. Open IntelliJ
    4. Choose **Import Project** option (instead of **Open**)
    5. Go through wizard and choose options that suites your projects needs.
