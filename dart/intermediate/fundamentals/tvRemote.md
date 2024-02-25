TV Remote

    int tv_remote(String word) {
      // Define the keyboard layout
      List<List<String>> keyboard = [
        ['a', 'b', 'c', 'd', 'e', '1', '2', '3'],
        ['f', 'g', 'h', 'i', 'j', '4', '5', '6'],
        ['k', 'l', 'm', 'n', 'o', '7', '8', '9'],
        ['p', 'q', 'r', 's', 't', '.', '@', '0'],
        ['u', 'v', 'w', 'x', 'y', 'z', '_', '/']
      ];
    
      // Initialize cursor position
      int cursorRow = 0;
      int cursorCol = 0;
    
      // Helper function to find character position on the keyboard
      List<int> findChar(String ch) {
        for (int i = 0; i < keyboard.length; i++) {
          for (int j = 0; j < keyboard[i].length; j++) {
            if (keyboard[i][j] == ch) {
              return [i, j];
            }
          }
        }
        return [-1, -1]; // Character not found
      }
    
      // Calculate the number of button presses
      int presses = 0;
      for (int i = 0; i < word.length; i++) {
        List<int> charPos = findChar(word[i]);
        int rowDiff = (charPos[0] - cursorRow).abs();
        int colDiff = (charPos[1] - cursorCol).abs();
        presses += rowDiff + colDiff + 1; // Move to the character and press OK
        cursorRow = charPos[0];
        cursorCol = charPos[1];
      }
    
      return presses;
    }
