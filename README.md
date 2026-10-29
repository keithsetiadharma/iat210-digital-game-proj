# Gurt: Digital Game Project (IAT 210)

**Group:** [group number]
**Members:** Andrew Vu, Keith Setiadharma, Mengna Ma, Xavier Sandilands
**Prototype version:** 0.1 (October 2026)

An interactive narrative in which you play Gurt before the events of *One Last Bounty*. Your choices change how the locals see Gurt, and they decide how the story ends. Built in Twine with SugarCube 2.37.3.

## How to launch
1. Unzip the folder.
2. Open `index.html` in Chrome, Firefox or Safari.
3. No install, login or internet connection is needed.

## Controls
- **Mouse:** click a link to make a choice.
- **Keyboard:** press Tab to move between links and Enter to select one.
- **Restart:** use the Restart button in the sidebar to go back to the starting state.

## Starting state (repeatable test)
Every load or restart begins at:
- Local Morale 0
- Security + Defence 0
- All flags false (incision, pendant, ulfAngry, built) and final choice none

No randomness is used, so the same choices always give the same result.

## Test it: choice sequences and expected endings
| Run | Choices | Final Morale, Security + Defence | Ending |
| --- | --- | --- | --- |
| 1 | Defuse, Tell her not to worry, Set up the defence system, Inspirational speech, Save the locals | 6, 5 | Ending 1 |
| 2 | Fight, Refuse, Save the locals | 7, 3 | Ending 2 |
| 3 | Fight, Refuse, Chase the Head Bandit | 7, 3 | Ending 3 |
| 4 | Defuse, Rub her back, Refuse, Chase the Head Bandit | 3, 0 | Ending 4 |

Ending rules: saving the locals gives Ending 1 if Security + Defence is above 4, otherwise Ending 2. Chasing the Head Bandit gives Ending 3 if Local Morale is above 4, otherwise Ending 4. Gurt becomes dictator of T'Chanui in every ending.

## Test question
**After you reach an ending, can you name the choice or choices that led to it?**

Please also tell us:
- Which ending you reached, and which choices you think caused it.
- Whether you replayed and changed a specific choice to get a different ending.
- Whether the Local Morale and Security + Defence numbers helped you understand why.

## Current limitations
- Passage text is **placeholder**. Only the structure and choices are final.
- There are no images, sound, or save and load. Restart and browser refresh are the only resets.
- The layout is built for desktop browsers and has not been tested on mobile.
- Some paths skip choices on purpose. For example, if Gurt fights, there is no Ulf choice, and the speech choice only appears if Gurt has the pendant.
- Accessibility checks (full keyboard-only pass and a screen reader pass) are still planned.
