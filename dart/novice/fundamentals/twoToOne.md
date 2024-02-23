Two to One

    String longest(String a, String b) {
      var combined = a + b;
      var distinctChars = combined.split('').toSet().toList();
      distinctChars.sort();
      return distinctChars.join('');
    }
