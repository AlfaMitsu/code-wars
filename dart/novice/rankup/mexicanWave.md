Mexican Wave

    List<String> wave(String str) {
      List<String> result = [];
      for (int i = 0; i < str.length; i++) {
        if (str[i] != ' ') {
          result.add(str.substring(0, i) + str[i].toUpperCase() + str.substring(i + 1));
        }
      }
      return result;
    }
