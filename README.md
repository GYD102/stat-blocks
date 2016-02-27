
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

   Shortcut to write "+mod to hit".

  Ex. input

    \toH{4}

  Ex. output

    +4 to hit

7) \reach{distance}

   Shortcut to write "reach distance ft."

  Ex. input

    \reach{10}

  Ex. output

    reach 10 ft.

8) \rangeOne{distance}

   Shortcut to write "range distance ft."

  Ex. input

    \rangeOne{100}

  Ex. output

    range 100 ft.

9) \rangeTwo{short}{long}

   Shortcut to write "range short/long ft."

  Ex. input

    \rangeTwo{150}{600}

  Ex. output

    range 150/600 ft.

10)\hitpoints{number}{die}{modifier}

   Writes a hit point maximum based on the number of dice, which die is used,
   and the modifier. For example, if the Monster Manual™ lists a creatures hit
   dice and modifier as being "2d12 + 4", use

    \hitpoints{2}{12}{4}

   Output:

    Hit Points: 30 (2d12 + 4)

11)\damage{number}{die}{modifier}{type abbreviation}

   Writes an average and rolled damage dice along with a damage type delt by an
   attack based on the dice rolled and modifiers added. For example, if an
   attack is listed as dealing "6d6 - 2 radiant" damage, use

    \damage{6}{6}{-2}{R}

   Output:

    26 (6d6 - 2) radiant damage.

12)Damage type abbreviations

   \damage command takes an abbreviation for damage type. If the damage type
   starts with an "F", write the first two letters of the damage type. If the
   damage type starts with a "P", write the first three letters of the damage
   type. Otherwise, only the first letter of the damage type is used.

   Acid: "A"

   Bludgeoning: "B"

   Cold: "C"

   Fire: "Fi"

   Force: "Fo"

   Lightning: "L"

   Necrotic: "N"

   Piercing: "Pie"

   Poison: "Poi"

   Psychic: "Psy"

   Radiant: "R"

   Slashing: "S"

   Thunder: "T"

Author & Contact
----------------
Glib Dolotov (gyd102@gmail.com)

Please use the above email to report bugs, suggest or request features, etc.
