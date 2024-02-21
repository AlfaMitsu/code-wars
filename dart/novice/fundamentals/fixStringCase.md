Fix String Case

    String solve(String s) {
      int uppercaseCount = s.split('').where((char) => char == char.toUpperCase()).length;
      int lowercaseCount = s.split('').where((char) => char == char.toLowerCase()).length;
      
      return uppercaseCount > lowercaseCount ? s.toUpperCase() : s.toLowerCase();
    }
