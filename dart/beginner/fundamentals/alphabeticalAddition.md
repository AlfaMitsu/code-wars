Alphabetical Addition

    String addLetters(List<String> letters) {
      if (letters.isEmpty) return 'z';
    
      int sum = letters.fold<int>(0, (acc, letter) => acc + (letter.codeUnitAt(0) - 'a'.codeUnitAt(0) + 1)) % 26;
      return sum == 0 ? 'z' : String.fromCharCode(sum + 'a'.codeUnitAt(0) - 1);
    }
