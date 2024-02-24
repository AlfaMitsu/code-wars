Stop Spinning my Words

    String spinWords(String str) {
      List<String> words = str.split(' ');
      for (int i = 0; i < words.length; i++) {
        if (words[i].length >= 5) {
          words[i] = words[i].split('').reversed.join('');
        }
      }
      return words.join(' ');
    }
