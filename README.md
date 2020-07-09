# MaxiTracker

This enables composing chiptunes in the style of the MSX-Music compatible MSX machines.

Two changes.
- "YM2413" instead of Konami VRC7
   - This is done by just changing the default patch set.
   - Only 6 melody channels are available. No rhythm channels.
- YM2149 (AY-3-8910) instead of Sunsoft 5B
   - This is done by removing the clock divider.
   
**To use YM2413 OPLL, select VRC7; to use AY/YM, select 5B.**

# Major functional limitations:

Names and labels have not been updated; PRs welcome.

Rhythm channels and 9ch support are not present, as the VRC7 did not have this enabled; PRs welcome.

Famicom compatibility and support has not been removed or hidden; PRs welcome.

Exports will continue to be for Famicom/NSF and VRC7/5B. They may be nonsensical; I recommend ignoring that function.

Audio reproduction should be accurate; otherwise, compatibility with a real MSX is null; PRs welcome.

If you want to playback on a real MSX machine, you're a masochist. Write a driver for NSF, or import from text export to VGM. Again, PRs welcome.

Other MSX sound chips, such as MSX-Audio, should be supported eventually. Please, PRs welcome.

VRC7 9 channel debug test register mode and the OPLL DAC test register are not supported or implemented. If you wish to do so, PRs welcome.

Nothing else is changed or removed from j0cc-FamiTracker, including instrument labels and expansion chip names. **PRs welcome.**

# Contributing

I will maintain this on an absolutely minimal basis; _please fork, improve, and contribute back._ I will accept sensible changes.

**The goal, and direction, of this project, is to support making music for the MSX.** 

Things which impede, imperil, or run counter to that goal, should be considered bugs.

Flaws with the MSX itself, or its user, are not a bug.


# Original source

This should be visible as a github Fork from j0cc-FamiTracker, at https://github.com/nyanpasu64/j0CC-FamiTracker.
