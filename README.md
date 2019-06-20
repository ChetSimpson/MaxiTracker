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

Nothing else is changed or removed from j0cc-FamiTracker, including instrument labels and expansion chip names. **PRs welcome.**

# Contributing

I will maintain this on an absolutely minimal basis; _please fork, improve, and contribute back._ I will accept sensible changes.

**The goal, and direction, of this project, is to support making music for the MSX.** 

Things which impede, imperil, or run counter to that goal, should be considered bugs.

Flaws with the MSX itself, or its user, are not a bug.

# jimbo1qaz 0CC-Famitracker

- Download at https://github.com/jimbo1qaz/0CC-FamiTracker/releases
- Dev builds at https://ci.appveyor.com/project/jimbo1qaz/0cc-famitracker/history

This is a fork of HertzDevil's 0CC-Famitracker 0.3.14.5 (since 0.3.15.1 and master are quite buggy and changing rapidly). It contains bugfixes which HertzDevil has not merged yet (some for months, some fixed independently in 0.3.15.1 or master), as well as N163 multi-wave copy-paste support.

Bugfixes:

- Export N163 FTI instruments properly.
- Don't corrupt memory when entering MML volume sequences over 252 items long (instead truncate).
- Fix bug where find-replacing anything with an empty effect creates " 00" effect.
- Fix text import instrument loop/release (@owomomo, fixed in 0.3.15.1).
- Update channel count after importing text (like master). Mark file as modified.

Enhancements:
- N163 file-specific mixing level offset.
- Typing Pxx (or FDS Zxx) defaults to P80.
- N163 wave editor's copy/paste buttons copy all waves at once, separated/terminated with semicolons. This allows for highly efficient Audacity-N163 import workflows (see https://gist.github.com/jimbo1qaz/424110eab84dad50cf1a6646a72b2627).
- Save TXT export path properly.
- Hi-res FFT spectrogram (like master).

Future changes:

- Exponential instrument volume decay or release (like ADSR), and possibly an effect.
- Warn when editing instrument sequences reused in many instruments, or patterns appearing in many frames.
- https://github.com/jimbo1qaz/0CC-FamiTracker/issues

# 0CC-FamiTracker

0CC-FamiTracker is a modified version of FamiTracker that incorporates various bug fixes and new features which work in exported NSFs as well. The name "0CC" comes from the author's favourite arpeggio effect command. The current version includes:

- Partial FamiTracker 0.5.0 beta support
- Sound engine extensions:
   - Ad-hoc multichip NSF export
   - Echo buffer access
   - Polyphonic note preview
- New effects:
   - Hardware volume envelope effects
   - Delayed channel effects
   - FDS automatic FM effects
   - N163 wave buffer access effect
- Instrument extensions:
   - Arpeggio schemes
   - Instrument recorder
   - Compatible sequence instruments
- Interface extensions:
   - Find / replace tab
   - Transpose dialog
   - Split keyboard
- Extra module contents:
   - Detune settings
   - Groove settings
   - Bookmark manager
   - Linear pitch mode

See the change log for the full list of changes made in 0CC-FamiTracker.

This program and its source code are licensed under the GNU General Public License Version 2. Differences to the original FamiTracker source are marked with "// // //"; those to the ASM source with ";;; ;; ;" and "; ;; ;;;".

The current build is based on the version 0.5.0 beta 5 release of the official FamiTracker. 0CC-FamiTracker will be ported to newer official releases once they become available; features added in 0CC-FamiTracker may not have identical behaviour as the corresponding features on the official branch.

# Links

- http://hertzdevil.info/programs/  
  The download site for all versions of 0CC-Famitracker.
- http://0cc-famitracker.tumblr.com/  
  The official development log of 0CC-FamiTracker.
- http://hertzdevil.info/bug/main_page.php  
  The official bug tracker for all of HertzDevil's programs.
- http://github.com/HertzDevil/0CC-FamiTracker  
  The Git source repository for the tracker (this page).
- http://github.com/HertzDevil/0CC-FT-NSF-Driver  
  The Git source repository for the NSF driver.
