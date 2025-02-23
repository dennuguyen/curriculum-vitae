# CV

```bash
# fix for unknown script 'mtx-context.lua' or 'mtx-mtx-context.lua'
mtxrun --generate

# build pdfs
context cv.tex
```

> https://wiki.contextgarden.net/Main_Page

## script.py

Generates alternative CVs based on tags beginning with `%!!!` preceding a heading.

If the tag exists on a subheading but not on the heading, then the heading is automatically included with the subheading.

Multiple tags can be applied to the list e.g. `[swe, comm]` to generate multiple alternative CVs.

An example tag on a heading will look like:
```tex
\CVSECTION{Education}
    %!!! [edu]
    \CVHEADING{UNSW}{2025}
        \CVSUBHEADING{Doctor of Philosophy}{}
    \CVHEADING{UNSW}{2020}
        %!!! [edu]
        \CVSUBHEADING{Bachelor of Engineering}{}
        \CVSUBHEADING{Bachelor of Computer Science}{}
```