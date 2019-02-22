-mackle todo
============

 - [ ] Replace .de with .Macro
 - [x] Superscript & subscript
 - [ ] Numbered lists
 - [x] Shunt pdf metadata initialization to its own (generic) macro
 - [x] Likewise shunt .Subject and .Keywords
 - [ ] Add outline and anchors per each header
 - [x] Columns support
 - [ ] Per-column footnotes
 - [x] Highlighting: .I, .B, .BI, .CW & similar
 - [x] Endnotes
 - [x] Autonumbering footnotes and endnotes
       Problem: autonumbering is done via macro, thus creating a break,
       thus leaving a space between the preceeding word and the note
       number.
 - [ ] Footnotes without numbers (e.g. `.Footnote *`)
 - [x] Headers and footers
 - [ ] Headers and footers for odd/even pages
 - [ ] Clean up the `st` module
 - [ ] Drop caps

paper document style
--------------------

Aims to be a replacement for the article LaTeX document class.

 - [ ] .Author should add to a stack, and more info to boot:
   - Full name
   - Given name
   - Family name
   - Title
   - Institution
   - Address

resume document style
---------------------

 - [ ] .Name, .Title
 - [ ] .Address, .Phone, .Email, .Website
 - [ ] .Introduction (akin to .Abstract)
 - [ ] .Section, .Subsection (.Header 1 and 2)
 - [ ] .Education
 - [ ] .Job
 - [ ] .Skillset

Sample resume:

```troff
.Resume
.PaperSize A4
.MainFont  Palatino
.Name      "Jane Doe"
.Title     "System Administrator"
.Address   "Somewhere" \
           "Over the rainbow"
.Email     "jane@doei.sh"
.Start

.Section Education
.Education "Oct 2003#Present" "President of something" \
           "Hello World, Inc." "Somewhere, CA"
Did so and so, it was great.
./Education

.Section Work Experience
.Job ...
Did so and so, it was great.
./Job

.Section Skills
.Skillgroup Programming languages
C/C++, C#, Perl, Python, Unix shell
./Skillgroup
.Skillgroup Languages
English, Even more English
./Skillgroup

.Section Publications
.R1
bibliography biblio.txt
.R2
```

letter document style
---------------------

 - [ ] .To, .From
 - [ ] .PS in lieu of footnotes (.PostScriptum would be a type of end
       notes, without as many complications as footnotes)
