# dndrc
DnD 5e Bashy Character Sheet

to start run `source .dndrc` from project root directory 

use the same format for character sheet file as other `*.dnd` files

run by entering the command and the character name in the same line

Installation:

Add the following to your .bashrc

```
dndrc_path="/path/to/dndrc"

function dnd() {
        echo "Applying dndrc..."
        source $dndrc_path/.dndrc
        cd $dndrc_path/$1
        if [ ! -z "$2" ]
        then
                echo "Booting up $1's $2"
                $2 $1
        fi
}

```

activate dndrc via command dnd. example

`dnd Podhl stats`

Commands:

`abs` - List character's abilities

`desc` - List character's description

`eq` - List character's equipment

`stats` - List character's stats

`combat` - List character's combat modifiers

`prof` - List character's proficiencies

example usage

`$ abs Podhl`
```
-- Podhl's Abilities --
+ Firbolg Magic (use Wisdom)
 + Detect Magic
 + Disguise Self - can appear 3ft shorter
+ Hidden Step - Bonus action; magically invisible until next turn, damage roll, or force saving throw; reuse after short/long rest
+ Powerful Build - One size larger when determining carrying capacity and weight I can push, drag, or lift
+ Speech of Beast and Leaf - One way communication with beast and plants; they can understand me but not the other way around; Advantage on Charisma checks to influence
+ Cantrip(s):
 + 1 - Thorn Whip
 + 2 - Shillelagh
+ Spell(s)
 + 1st Level
   + 1 - Cure Wounds
   + 2 - Thunderwave
```
