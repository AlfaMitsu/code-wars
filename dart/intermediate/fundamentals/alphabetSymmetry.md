Alphabet Symmetry

    List<int> solve(List<String> arr) {
      int alphabetPosition(String letter) {
        return letter.codeUnitAt(0) - 'a'.codeUnitAt(0) + 1;
      }
    
      List<int> result = [];
      for (String word in arr) {
        int count = 0;
        for (int i = 0; i < word.length; i++) {
          if (alphabetPosition(word[i].toLowerCase()) == i + 1) {
            count++;
          }
        }
        result.add(count);
      }
      return result;
    }
