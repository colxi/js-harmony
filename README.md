# js-harmony

js-harmony library is a set of **musical related methods and definitions**, dessigned to generate **Notes, Intervals, Chords and Scales**.
It provides some custom Objects types, and validations functions. The supported structures and types are are the following :

- **Intervals** : 'dim' | 'm' | 'P' | 'M' | 'aug'
- **Chords** : 'major' | 'minor' | 'dim' | 'aug' | 'max7'| 'm7' | '7' | 'semidim'
- **Major Scales** : 'ionian'
- **Minor Scales** : 'aeolian' | 'harmonic' | 'bachian' | 'melodic'
- **Modes**: 'ionian' | 'dorian' | 'phrygian' |	'lydian' |	'mixolydian' |	'aeolian'	|	'locrian' 

### Usage :

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
- `makeInterval` : ƒ (grade, quality, direction, root)
- `makeIntervalNote` : ƒ (grade , quality, direction, root)
- `makeScale` : ƒ (mode,name,root)
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
