Vowel Count

    int getCount(String inputStr) {
      return inputStr.split('').where((char) => 'aeiou'.contains(char)).length;
    }
