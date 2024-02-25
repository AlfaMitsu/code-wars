Consecutive letters

    bool solve(String s) {
      // Sort the string to ensure letters are in order
      List<String> sortedString = s.split('')..sort();
    
      // Check if each letter occurs only once
      if (sortedString.length != sortedString.toSet().length) {
        return false;
      }
    
      // Check if the difference between consecutive characters is always 1
      for (int i = 1; i < sortedString.length; i++) {
        if (sortedString[i].codeUnitAt(0) - sortedString[i - 1].codeUnitAt(0) != 1) {
          return false;
        }
      }
    
      return true;
    }
