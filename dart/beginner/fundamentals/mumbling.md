Mumbling

    String accum(String str) {
      return str.split('').asMap().entries.map((entry) {
        int index = entry.key;
        String letter = entry.value;
        return letter.toUpperCase() + letter.toLowerCase() * index;
      }).join('-');
    }
