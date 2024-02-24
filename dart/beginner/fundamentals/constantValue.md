Constant Value

    int solve(String s) {
      final consonants = 'bcdfghjklmnpqrstvwxyz';
      final values = Map.fromIterable(consonants.runes.toList(),
          key: (c) => String.fromCharCode(c), value: (c) => c - 'a'.codeUnitAt(0) + 1);
    
      final groups = s.split(RegExp('[aeiou]+'));
      final sums = groups.map((group) => group.runes.map((c) => values[String.fromCharCode(c)]!).fold(0, (a, b) => (a as int) + b));
      return sums.isNotEmpty ? (sums.reduce((a, b) => a > b ? a : b) as int) : 0;
    }
