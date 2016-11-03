Requirements
=======================================

**Introduction**

First the team each read through the brief and associated documentation.
Then we got together and discussed our ideas, coming up with a rough
draft of some basic and some more advanced requirements. From these we
discussed the more ambiguous points, such as what sort of view the
player will use, and where the murder will take place. From these we
picked out the most ambiguous parts that prevented us from continuing
with basic designs and discussed them with our customer. After two
interviews with our customer we finalised the requirements.

At the first group meeting we decided to play cluedo to get a feel for a
general detective game. This sparked great discussion, and allowed for
great strides to be made on requirements very early on, by giving us an
idea of what works in a game. This also allowed us to discuss ideas that
would be interesting but more difficult to implement, which we left as
possible expansion if overall time costs do not overrun.

After discussing our ideas on clues for a bit, as a group we decided
that the most effective way of deducing the murderer was to attempt a
‘guess who’ style. This way the player can cross off certain characters
upon finding clues that confirm their alibis. This should allow the
player to feel as though they are actually solving the crime, rather
than just witnessing the solving.

The tables below are numbered using the following system:

The first number is category (The bit in bold e.g. Characters)

The second number represents ‘must(1), should(2), could(3)’ (the
priority of achieving the

requirement)

The third number is the requirements position in the list (to make it
easier to find and refer to)

The numbering is spread across the two tables.

The requirements are sorted into two tables, functional and
non-functional. Functional requirements are things that the system does,
so mainly requirements for when the game is running. Non-functional
requirements are things that the system is, so mainly qualities the game
must have, or objects that are hard coded.

The requirements are laid out in tables for ease of access. By giving
each requirement a row and a number all information is easy to find
quickly in future. Any and all associated risks are discussed in the
risks document.

Some requirements are based on considerations of environmental
assumptions of the game. for example, a ‘colour-blind’ option is listed
below (6.3.2) due to the possibility that a person wanting to play the
game cannot see some colours. Requirements based on hardware have all
taken into account the systems that the game is designed to run on.

**Functional Requirements**

\|No.\|Requirement\|Success Criteria\|Alternative Requirements\|
\|Characters\| \|1.1.1\|The murderer and victim must be randomly
selected each time the game begins from two sub-lists of murderers and
victims.\|Upon loading the game at least 2 times either or both the
victim and murderer will change.\|N/A - necessary requirement.\|
\|1.1.2\|The NPCs must spawn randomly into rooms so that each room has
at least one NPC at the start of the game.\|Upon loading of the game the
NPCs will be spread around the map so that there is no room without an
NPC.\|We will have to rotate where the NPCs spawn.\| \|MAP\|
\|2.1.1\|Rooms on the viewable map must be revealed only once the player
has visited the respective rooms.\|Walk through map and check that rooms
are only revealed once visited.\|All of the map will be visible from the
start.\| \|DIALOGUE/INTERACTION\| \|3.1.1\|The player must always get
three choices of interaction with NPCs - Question, Accuse and
Ignore.\|Ensure while game is running the player can use any of these
interactions with NPCs.\|N/A - necessary requirement.\| \|3.1.2\|All
dialogue must change based on the characteristics of the player
character and NPC.\|With different previous interactions, conversations
between NPCs and the player change.\|Each character has set lines of
dialogue.\| \|3.1.3\|The game should have a method, for example a button
at the side of the game, to allow the player to view the map, character
sheets, clues found and other points of interest.\|Check functionality
as described throughout a play-through.\|N/A - otherwise the player
cannot review information collected.\| \|Clues\| \|4.1.1\|Clues must
help with the elimination process, but some will point to more than one
character.\|Ensure that all clues look meaningful, but some have false
assumptions associated with them.\|N/A - clues are necessary.\|
\|4.1.2\|The murder weapon must be found before the player is able to
accuse any NPCs.\|Make sure the player cannot accuse NPCs before they
have found the murder weapon.\|Murder weapon does not have to be found
before the player is able to accuse NPCs.\| \|Score\| \|5.1.1\|The score
must be raised when a clue is found.\|If the player finds a clue, the
score is raised.\|There will be no scoring.\| \|5.1.2\|The score must be
lowered for each wrong accusation and each question asked.\|The score
changes as required.\|There will be no scoring.\| \|5.3.1\|The player
could start with a predetermined score which is reduced for each second
played.\|Check that score reduces as time is spent playing the
game.\|There will be no scoring.\| \|Other/System\| \|6.3.1.1\|IF the
game has a soundtrack it must have a ‘sound on/off’ option.\|Check that
sound turns on/off when appropriate option chosen.\|The game will have
no soundtrack.\| \|No.\|Requirement\|Success Criteria\|Alternative
Requirements\| \|Characters\| \|1.1.3\|The game must have a cast of 10
NPCs (Non-Player Characters).\|The game contains 10 NPCs.\|N/A -
necessary requirement.\| \|1.1.4\|The murderer must have a motive that
becomes clear at some point in the game, not necessarily before they are
accused.\|Game functions as described.\|The murderer will not have a
clear motive.\| \|1.1.5\|There must be a narrator who acts as the
tutorial and further help during gameplay.\|The narrator talks to the
player.\|There will be no narrator.\| \|MAP\| \|2.1.2\|The game must
contain a game-map of 10 separate rooms, spread across the setting of
‘The Ron Cooke Hub’.\|The game will have 10 rooms.\|N/A - necessary
requirement.\| \|2.2.1\|The room of the crime scene/murder room must be
chosen randomly each time the game begins.\|Upon loading the game at
least 2 times the murder room will change.\|The crime scene is always in
the same place.\| \|Dialogue/Interaction\| \|3.1.4\|The game must have
multiple ‘plot lines’.\|Play through the game multiple times, checking
that the plot lines differ each time.\|N/A - necessary requirement.\|
\|3.2.1\|Some plotlines could be more intricate than others.\|Play
through the game and determine that some plotlines are more
complicated.\|The game line has similar plot lines.\| \|Clues\|
\|4.1.3\|There must be at least one clue to find in each room on the
map.\|Make sure that clues spawn in each room.\|N/A - necessary
requirement.\| \|4.2.1\|Some ‘constant’ clues should be available, for
example the guest sign in book in the central part of the map.\|Check
that consistent clues spawn in the correct place on at least 2 separate
occasions.\|There are no ‘constant’ clues.\| \|4.2.2\|Some rooms should
have more than one clue e..g note left by victim/murder weapon.\|Check
that at least one room has at least one clue in.\|There is only one clue
per room\| \|4.3.1\|The player could be able to interact with or pick up
some items which are not clues.\|Check the player can interact with some
item and it not be listed as a clue.\|All clues will be meaningful.\|
\|Score\| \|5.1.3\|The player must be scored on time taken, number of
wrong accusations, number of questions asked and number of clues
found.\|Play through the game at least 3 times to check that scores add
up as expected.\|There will be no scoring system.\| \|5.3.2\|A list of
high-scores could be stored on a server.\|Check the server contains the
high scores.\|There will be a local list of high scores or no list of
high scores.\| \|Other/System\| \|6.1.1\|The game will be controlled by
\_\ **XXXXXXXXX**.\|Determine the game is controlled as described.\|N/A
- necessary requirement.\| \|6.1.2\|The game must play on a windows
based system.\|Determine the game runs on the system described.\|N/A -
necessary requirement.\| \|6.1.3\|The game must be played in a ‘top
down’ viewpoint, where the player is in the centre of the screen and the
world moves around the player. The viewpoint is fixed zoom.\|Check the
game is viewed as described.\|The game will be played in an improved
viewpoint based on the reason for discarding this one.\| \|6.2.1\|The
game should run smoothly on university computers.\|Use frame-rate
measuring software to obtain a frame-rate of at-least 30.\|N/A -
necessary requirement.\| \|6.3.1\|The game could have a
soundtrack.\|Check that sound plays when game is running.\|The game will
not have a soundtrack.\| \|6.3.2\|The game could have a ‘colour blind’
setting.\|When activated, the colourblind setting changes all textures
in the game to ones that are easier for a colour-blind person to
see.\|The game textures will be designed with colour blindness in
mind.\| \|6.3.3\|The game could be cross compatible on mobile (android)
and Mac.\|Make sure game runs on alternative systems.\|The game will not
be cross compatible.\|