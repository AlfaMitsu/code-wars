Word values

    List<int> wordValue(List<String> arr) {
      int calculateStringValue(String str) {
        int value = 0;
        for (int i = 0; i < str.length; i++) {
          if (str[i] != ' ') {
            value += str.codeUnitAt(i) - 'a'.codeUnitAt(0) + 1;
          }
        }
        return value;
      }
    
      return arr.asMap().entries.map((entry) => calculateStringValue(entry.value) * (entry.key + 1)).toList();
    }
