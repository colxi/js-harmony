# js-harmony

JSHarmony library is a set of musical related methods and definitions, dessigned to generate Notes, Intervals, Chords and Scales.
It provides some custom Objects types, and validations functions.

### Constructors:
makeChord : ƒ (root, type)
makeChordFromGrade : ƒ (tonallityRootNote,grade,mode,triad_FLAG)
makeInterval : ƒ (grade, quality, direction, root)
makeIntervalNote : ƒ (grade , quality, direction, root)
makeScale : ƒ (mode,name,root)
getChordTypeFromGrade : ƒ (grade,mode,triad_FLAG)
getGradeMode : ƒ (grade,mode)

### Validators:
isAccidentalsArray : ƒ (array)
isArray : ƒ (obj)
isChordName : ƒ (chordName)
isInt : ƒ (integer)
isMode : ƒ (mode)
isNote : ƒ (noteObj)
isNoteArray : ƒ (array)
isNoteName : ƒ (note)

### Definitions :
def : {scale: {…}, accidentals: {…}, intervals: {…}, scales: {…}, modes: {…}, …}

### Misc :
objType : ƒ (obj)
randomBoolean : ƒ ()
randomChord : ƒ (root,type)
randomKey : ƒ (array)
randomNote : ƒ (name, accidentals, octave)
scaleExist : ƒ (mode,scale)
toNotesArray : ƒ (notesHandler)
