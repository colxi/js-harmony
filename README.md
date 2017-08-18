# js-harmony

js-harmony library is a set of **musical related methods and definitions**, dessigned to generate **Notes, Intervals, Chords and Scales**.
It provides some custom Objects types, and validations functions. The supported structures and types are are the following :

- **Intervals** : 'dim' | 'm' | 'P' | 'M' | 'aug'
- **Chords** : 'major' | 'minor' | 'dim' | 'aug' | 'max7'| 'm7' | '7' | 'semidim'
- **Major Scales** : 'ionian'
- **Minor Scales** : 'aeolian' | 'harmonic' | 'bachian' | 'melodic'
- **Modes**: 'ionian' | 'dorian' | 'phrygian' |	'lydian' |	'mixolydian' |	'aeolian'	|	'locrian' 

### Package distribution networks :

In **browser** enviroment you can include this library using the jsdelivr CDN ...

`<script src='https://cdn.jsdelivr.net/gh/colxi/js-harmony@1.4/js-harmony.min.js'></script>`

If you are in the **NodeJs** enviroment, can install the package via:

`npm install js-harmony`

---

### Usage :
All the available methods of the library underlie on the main JSHarmony Object. 
(**Note**: the JSHarmony.makeNote() method could be considered the starting point of most of the interactions with the Library)

```javascript
var cNote = JSHarmony.makeNote("C##8");
/* OUTPUT -> 
Note{
  name: "C", 
  accidentals: ["#" , "#"], 
  octave: 8, 
  duration: 1
}
*/

var cMinorChord = JSHarmony.makeChord(cNote, "minor");
/* OUTPUT -> 
Chord{
  type : "minor",
  notes: [
    Note{ name:"C", accidentals:["#", "#"], octave:"8", duration:1 },
    Note{ name:"E", accidentals:["#"], octave:"8", duration:1 },
    Note{ name:"G", accidentals:["#", "#"], octave:"8", duration:1 }
  ]
}
*/
```

### Constructors:
Will return an Object containing the requested Item
- `makeNote` : ƒ (noteName)
- `makeChord` : ƒ (rootNote, type)
- `makeChordFromGrade` : ƒ (tonallityRootNote,grade,mode,triad_FLAG)
- `makeInterval` : ƒ (grade, quality, direction, rootNote)
- `makeIntervalNote` : ƒ (grade , quality, direction, rootNote)
- `makeScale` : ƒ (mode,name,rootNote)
- `getChordTypeFromGrade` : ƒ (grade,mode,triad_FLAG)
- `getGradeMode` : ƒ (grade,mode)

### Validators:
Will help to identify or check some qualities or types about the provided items
- `isAccidentalsArray` : ƒ (array)
- `isChordName` : ƒ (chordName)
- `isMode` : ƒ (mode)
- `isNote` : ƒ (noteObj)
- `isNoteArray` : ƒ (array)
- `isNoteName` : ƒ (note)

### Definitions :
Some internal musical definitions, structures, and academic standards and conventions
- `def` : {scale: {…}, accidentals: {…}, intervals: {…}, scales: {…}, modes: {…}, …}

### Misc :
Many general prupose methods, and randomizers. 
- `objType` : ƒ (obj)
- `randomChord` : ƒ (root,type)
- `randomKey` : ƒ (array)
- `randomNote` : ƒ (name, accidentals, octave)
- `scaleExist` : ƒ (mode,scale)
- `toNotesArray` : ƒ (notesHandler)

### License
----

GPL
