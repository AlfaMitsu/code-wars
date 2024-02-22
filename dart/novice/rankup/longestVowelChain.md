Longest Vowel Chain

    int solve(String s) {
      int longestLength = 0;
      int currentLength = 0;
    
      for (int i = 0; i < s.length; i++) {
        if ('aeiou'.contains(s[i])) {
          currentLength++;
          longestLength = currentLength > longestLength ? currentLength : longestLength;
        } else {
          currentLength = 0;
        }
      }
    
      return longestLength;
    }
