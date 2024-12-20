# Matters Of State by Shiny Dorky
 ver 1.0A
## Overview

Matters Of State is a CK3 mod that aims to expand mechanics connected to governing your realm. 
It currently lets you do so mainly by giving you access to new laws, which once passed will be applied 
to all in your realm.

DISCLAIMER: I am not a historian, and this is not meant to be an accurate representation of political and
socioeconomic conditions of medieval world. Especially anything west of Urals and south of Sahara - I am by no 
means an expert.
This mod intends to just add some more layers to gameplay and I am just one guy. 
If sufficient interest will be expressed, I may recruit some people to help with creation
of this mod - historicity included. For now this is just a passion project.

## Mechanics

### Reforms

Reforms form the backbone of this mod. They provide modifiers or enable certain actions. Usually they can
be implemented only by independent rulers, and their effects will apply to all in the realm. AI is also
able to implement them.
#### Opening reform window
Reform window is opened using a button placed on the right side of your screen. It is visible 
only when one of sidebar tabs is open. This is done to reduce chance of clipping with existing UI or
other mods.

![Obraz ](screenshots/closed_reform_window.jpg?raw=true "Title")

#### Major reforms
Major reforms are placed on top of their respective tabs. In most cases passing them is necessary
to pass more advanced reforms from the same category. Those reforms are locked behind government types
and require gold to pass, cost of which scales with realm rank and size. Major reform levels can also be
lowered in order to obtain a temporary cash boost, but doing so will instantly invalidate all minor reforms
requiring previous level and assign lower tier, usually less beneficial reforms. After passing either
lower or higher reform, player is not able to do so again for a period of three years.

![Obraz ](screenshots/block_reform_tribal.jpg?raw=true "Title")

#### Minor reforms
Minor reforms do not cost gold to pass and have separate cooldown, lasting only six months. On the other
hand, while major reforms are almost always purely beneficial, minor reforms are usually tradeoffs of some
kind. As written previously, they usually require corresponding major reform to be passed before progressing
further. That is not always the case, and work is being done to differentiate those reforms graphically.

Minor reforms do not always force linear progression - if a reform set doesn't have a thread in the 
background, that means that you do not need to have a neighbouring reform in order to pass any of the others.

![Obraz ](screenshots/reforms_view_econ.jpg?raw=true "Title")

## Compatibility

At current state, MOS should be fairly compatible with almost any other mod with 
one notable exception - those that modify the `my_realm_window.gui` file. 

Writing a compatch should be relatively easy - all modified files are listed in `overwrites.info` file.
Each modification to the file is wrapped in `### MOS ###` and `### /MOS ###` comments. Copy and paste them
to corresponding places in overwriting mods and everything should work.

## Writing submods

You are free to write submods using my framework as long as I am credited and as long as they noticeably
expand functionality of the mod, whether it is by adding new mechanics or by translating. I do not allow any 
outright reposting of this mod without my consent.

While adding new mechanics, I will strive to provide `.info` files in appropriate places in order to
make it easier to tweak the mod on your own.

## Plans for the future
What I am planning to do with the mod. This is a very rough outline. All of this is a subject to change. ESPECIALLY if
Paradox release a DLC which invalidates on of the stated goals or breaks previously implemented features.

### Graphics - Expected: 10.01.2025 - Ongoing
Planned:

#### Replacing repeating assets
For now the mod uses the same graphics set for all reforms - that won't do.

As I am not particularly gifted when it comes to creating art, I will strive to use as much the GFX provided
in game files as possible. In other cases it will be either something bought/found in the internet or my 
own attempts at creating a placeholder until something better is found. I do not plan to use AI 
generated graphics in this mod.

### Through Thick and Thin - Expected: 30.01.2025
An expansion focused on creating more opportunities for either achieving prosperity and losing balance in order
to prevent Super Blobs from taking over the world and help smaller states survive.

Planned:

#### Administrative limit
A new mechanic modeled loosely on EU4 admin limit. Said limit will be increased by passing major administrative revolts.
It's usage will depend on size of your territory and tier of some passed reforms (like education for instance).

Once surpassed, progressively more punishing modifiers will be applied, which will force the ruler to slow down
and consolidate before continuing their conquest.

Usage of administrative limit will be lowered by new "Vassal Autonomy" reforms, which will decrease obligations of your
vassals in exchange for reducing the strain their lands put on your administration. Said laws do however carry a 
certain risk, which will be explained in the next section:

#### Incidents
Incidents will be a special type of event chains - they will be able to trigger once certain conditions are
fulfilled and they will culminate in a major modifier or event. Players will be shown their ongoing incidents
and ways of preventing them in a new `Incident View` window.

Incidents not be exclusively detrimental. They may lead to positive outcomes and in such cases it will be in player's
interest to avoid actions which would stop them.

Some planned negative incidents:
- Great Revolt - If vassals are not kept in line, some of them may get ideas.
  - Triggered by an independent ruler having strong vassals at max autonomy for too long,
  - A vassal will be chosen (with first choice being offered to player) to lead a rebellion against their liege,
  - Instead of normal rebellion, an empire or kingdom de jure above vassal will be given to them and all neighbours
  will be invited to join it, with decision being based among others on opinion and cultural acceptance,
  - Should revolt win, they will become independent and loser's state will be temporarily crippled,
  - Should liege win, they will confiscate all titles of rebellious vassals and receive timed modifier,
  decreasing their administrative limit usage
  - No white peace - rebels are all in, and they know it.
- Moment of Opportunity - Strong army means safe ruler, weak army means new ruler.
  - Triggered by having a weak army and low legitimacy,
  - Vassals will get progressively more annoyed,
  - Ambitious vassals may start to get claims on your title/titles

Some planned positive incidents:
- Military Excellence - I have no moderately amusing line to put here.
    - Triggered by having a big army and long period of peace,
    - Outcomes partially dependent on marshal and most militarily skilled vassals,
    - Provides temporary bonuses to army
    - May end up passing a higher military law for free if not at max
    - Will grant a decent chunk of gold otherwise
- Education for The Masses - .
    - Triggered by high popular opinion in realm and having at least Local Schools reform,
    - Outcomes partially dependent on other passed reforms and steward,
    - Will allow to spend money in order to expand basic education system
    - All counties in realm will be given modifier reducing their taxes and increasing dev growth along with popular
  opinion,
    - Ruler will be given option to abolish the expanded schooling - modifier will be removed

### Princes and Senators - Expected: TBD
An expansion focusing on creating mechanics modeled on the assemblies present in many medieval states, like imperial
diets or germanic things. Their existence will serve to add more variety to vassal side of gameplay.

While starting out as mainly advisory bodies, called upon whenever liege wishes, those assemblies may morph into bigger
institutions and assume more and more responsibilities - such as passing laws, reforms and declaring law.

Rulers will be able to solve many problems by summoning those assemblies - they will be able to lower tensions in realm,
pass extraordinary taxes and request help in war. Every use of this instrument however may give some funny ideas to
their vassals, which will be represented using Incident mechanic. Once it happens, struggle for state authority will
begin.

#### Unique variants
I intend to make some unique variants of these assemblies, depending on country, culture, etc.
There are no concrete plans for now but I am reasonably sure that germanic things and imperial diets
will be considered.