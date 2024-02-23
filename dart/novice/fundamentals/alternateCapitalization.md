Alternate Capitalization

    List<String> capitalize(String s) {
      String even = s.split('').asMap().entries.map((entry) => entry.key % 2 == 0 ? entry.value.toUpperCase() : entry.value).join('');
      String odd = s.split('').asMap().entries.map((entry) => entry.key % 2 != 0 ? entry.value.toUpperCase() : entry.value).join('');
      return [even, odd];
    }
