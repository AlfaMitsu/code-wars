Sum of a Beach

    int sumOfABeach(String str) {
      var words = ["sand", "water", "fish", "sun"];
      var count = 0;
      for (var word in words) {
        var pattern = RegExp(word, caseSensitive: false);
        count += pattern.allMatches(str).length;
      }
      return count;
    }
