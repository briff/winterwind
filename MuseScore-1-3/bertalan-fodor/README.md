# openLilyLib Engraving Challenges

## Challenge #02 - Chopin/Godowsky

### LilyPond development version

This document will be the report of tackling the Chopin/Godowsky challenge
with the stable version of
[MuseScore 1.3](http://musescore.org)
I'm working on a small netbook with no mouse, so I might be slower than being on a big workstation, but that's my problem :)

#### Analysis
- The score seems somewhat complicated, so I think I will have to rely on many manual adjustments and some drawing as well
- I don't think that the nonstandard beaming is supported by MuseScore. First I will create that before the full raw note entry, as first I want to know how I'll do that.
The solution can affect how I typeset the raw notes.
- So first I did the first bar right hand first 3 quarters
- I spent cca. 30 minutes about experimenting with a solution to do the non-standard beaming. I think I will rely on putting in white boxes when everything is ready
as the slope of the beam can change.
- I just realized that they are note quarter notes, but tuplets...
- Anyway, probably I will do some tricks with moving manually 8th notes and 16th notes to have correct beaming, keeping only the beam visible. That will need manually
setting the slopes as well... it won't be a fast process and must be done when the line breaks and every positions are fixed
- In measure 6 there is a strange use of tuplets, so I have to be quite careful

#### Note entry
- The first deep note was written by just counting the ledger lines -- I didn't know what note is that :)
- The second voice rests had to be made invisible
- Measure 3 and 4 right hands are quite similar, so I added all the articulations and dynamics etc. in this phase to allow me copy and paste
- The slurs had to been flipped, just as the beams' direction
- In measure 5 I turned off the tuplet numbers and brackets
- Measure 6: a half-note made into 6-et
- Started voice 2 - terrible collisions... :(
- Put in a spacer in bar 6 as I just couldn't see anything :)
- After an hour of work, I think most of the notes are there, but now everything is so collided that I decided to start from the first measure and clean everything up, 
hiding invisible elements and adding spacers to avoid the most annoying collisions
- Measure 4 adding other voices: switching between 1st and 2nd voices here and there to allow collision detection and the tie in right hand last note
- It is very annoying that musescore jumps to the next page... but Sibelius would do the same :) and had I a bigger screen...
- Adding articulations and symbols - I move Ped symbols now to allow copy&pasting the changed location as well
- Default fingering positions are awful, changing a bit just to let me see the numbers. Later I'll move them manually and change their font.
- In bar 3 there are some double fingerings, so I moved them away now, because later even selecting them would be hard
- Same for articulation marks: I moved them to more easy tweaking later
- I can add symbols to symbols, so I can copy and paste the parenthesized (Ped) sign
- I'm at around 2 hours of work
- There are some alternative fingerings: I add both of them, but with offset
- After another 30 minutes, I'm at the end again, after adding all fingerings and probably all symbols.
- But is very hard to go over and over the score, so now I'm doing measures one by one. (Keeping only the special beaming to the end of the whole process.)

#### Making position adjustments measure by measure
##### M1
- moved meno F and changed to italic
- moved staccato notes manually with the keyboard and the mouse (in the last case, as due to some strange MuseScore beavior, changing the dot position changed the 
accent mark as well) 
- changed dim. and made it italic

##### M2
- Added spacer
- Added hairpins, second aligned by hand
- Moved articulations
- Switched to tight spacing. Doesn't help, I reduce the sizes instead. I would like to get the first two bars in the same line.
- With an 1.5mm spacing everything fits quite right, though i have to reposition the manually adjusted symbols.
- Selected all Fingering elements, then change their font to MScore1 8pt
- In this version of MuseScore vertical positioning of fingering is only possible with the mouse, so I tried to line them up viewing with large zoom

##### M3
- Manually edited the first righthand slurs - luck that I have a hand engraved score to look at, otherwise it would be hard to find a good looking shape (it's still hard this way)
- To my surprise MuseScore 1.3 doesn't support rotating the hairpin. So I'm drawing this with 2 normal lines - fortunately normal lines can be attached to note positions as well.
-- An annoying bug made it somewhat hard - selection is based on bounding box (at least for beams and lines, and I just couldn't select what I wanted)
- I wanted to fix the cross staff beam slant, but again a bug in MuseScore 1.3 - If you change anything it is incorrectly drawn
- Added the left hand crescendo hairpin manually drawing 2 lines - I think literally drawing stuff on a score makes it more beautiful, as it is really hand "engraved"
- arount 160 minutes of net work now
- The line between fingerings are simple _ character in a separate text item
- 10 minutes later...

##### M4
- Same as previous
- 25 minutes

##### M5
- Funny collision avoiding in F#
- Avoided collisions in first part of measure 5 by moving things around, also changed slurs
- The dot should be moved in the fs8. in the right hand, but in MuseScore this is not possible. The workaround I used:
-- Make the notehead and the dot invisible
-- Add a notehead symbol to the invisible notehead - it will appear just at the right place
-- Add a dot symbol
-- 20 minutes

#### M6
- Nothing new - had to touch almost every symbol though
- 10 minutes

#### M7
- Fixed 8va, set as dotted
- Fixed stem directions
- Fixed symbol positions
- Added parentheses
- 5 minutes

#### M8
- Trick at the end: hidden beam, moved every note right 1 bit step and 4 small steps to align with left hand.
- I didn't want to add one more bar, so just changed ending barline, added extra space after last note and added an F-clef symbol
- 5 minutes
- I couldn't find a add a big nice musical parenthesis, so I used the one from the text font
