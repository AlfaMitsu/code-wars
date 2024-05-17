Piano Kata Part 2

    package kata
    
    func WhichNote(keyPressCount int) string {
        notes := []string{"A", "A#", "B", "C", "C#", "D", "D#", "E", "F", "F#", "G", "G#"}
        
        // Calculate the position within the 88 keys
        position := (keyPressCount - 1) % 88 + 1
        
        // Calculate the note index within the 12-note cycle
        noteIndex := (position - 1) % 12
        
        // Return the corresponding note
        return notes[noteIndex]
    }
