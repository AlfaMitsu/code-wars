Roman Numerals Decoder

    int romanToInt(String s) {
      Map<String, int> romanValues = {
        'I': 1,
        'V': 5,
        'X': 10,
        'L': 50,
        'C': 100,
        'D': 500,
        'M': 1000
      };
    
      int result = 0;
      for (int i = 0; i < s.length; i++) {
        int currentValue = romanValues[s[i]]!;
        int nextValue = i < s.length - 1 ? romanValues[s[i + 1]]! : 0;
    
        if (currentValue < nextValue) {
          result += nextValue - currentValue;
          i++;
        } else {
          result += currentValue;
        }
      }
    
      return result;
    }
