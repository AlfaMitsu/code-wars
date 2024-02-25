Bases Everywhere

    int base_finder(List<String> seq) {
      Set<String> uniqueDigits = {};
      for (String num in seq) {
        uniqueDigits.addAll(num.split(''));
      }
      return uniqueDigits.length;
    }
