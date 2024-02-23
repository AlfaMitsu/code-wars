Counting Duplicates

    int duplicateCount(String text) {
      var charCount = <String, int>{};
      var duplicates = 0;
      
      for (var char in text.toLowerCase().split('')) {
        charCount[char] = (charCount[char] ?? 0) + 1;
        if (charCount[char] == 2) {
          duplicates++;
        }
      }
      
      return duplicates;
    }
