
Stat Blocks
===========

Overview
--------
A means of generating creature stat blocks like those found in the
Dungeons & Dragons® Monster Manual™. Using the template and an example, it is
easier to create a .tex file for the desired stat block. This .tex file can
then be converted to a pdf using pdflatex or some other method for easy 
printing.

Key
---
\* - Planned changes, modifications, improvements

Files
-----
1) macros.tex (LaTeX macros that facilitate stat block generation)

2) template.tex (Sample and template for stat block .tex files)

3) sample.pdf (Sample; .pdf converted version of template.tex)

Usage
-----
1) Copy and rename 'template.tex' to serve as base file for desired stat blocks.
   Make sure to include 'macros.tex' in the same directory or else the .tex file
   will refuse to compile when a .pdf creation is attempted.

2) Rewrite all relevant information into the appropriate spots. I.e. replace
   '\creatureName{Hobgoblin}' with '\creatureName{}' and the name of your
   creature inside the braces.

3) Rewrite or add appropriate abilities or attacks using the macros written in
   'macros .tex'. (See "Macros" section for additional documentation.)

Macros
------
1) \stats{STR ability score}{DEX ability score}{CON ability score}
   	 {INT ability score}{WIS ability score}{CHA abiliiy score}

   Takes 6 ability scores and generates an appropriate ability table.

  Ex. input:
   
    \stats{20}{15}{13}{11}{8}{10}

   Ex. output:
   
     STR  DEX  CON  INT  WIS  CHA
     (+5) (+2) (+1) (0)  (-1) (0)

2) \creatureName{name}

   Takes a creature name and writes in in the appropriate typeface and size.
   See 'sample.pdf' and 'template.tex' for an example.

3) \ability{name}{detail}

   Writes the name in bold font and detail in standard font after. Used for
   first half of stat block (Armor Class, Hit Points, Speed, Skills, Damage
   Resistances, Condition Immunities, Senses, Languages, Challenge, etc.).
   See 'sample.pdf' and 'template.tex' for an example.

4) \action{name}{category}{detail}

   Writes the name in bold and italicized font, category in only italicized
   font, and detail in regular font. Useful for creature abilities and actions
   such as attacks, spells, etc. "Category" input is usually used for weapon
   attacks. If there is no italicized text after the action name, leave that
   input blank. See 'sample.pdf' and 'template.tex' for an example.

5) \mwa, \rwa, \morwa, \msa, \rsa

   Shortcut to write "Melee Weapon Attack:", "Ranged Weapon Attack:", "Melee or
   Ranged Weapon Attack:", "Melee Spell Attack:", and "Ranged Spell Attack:"
   accordingly.

6) \toH{modifier}

   


Author & Contact
----------------
Glib Dolotov (gyd102@gmail.com)

Please use the above email to report bugs, suggest or request features, etc.
