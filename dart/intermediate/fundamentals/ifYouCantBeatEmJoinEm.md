If you can't beat 'em, join 'em!

    List<int> cantBeatSoJoin(List<List<int>> gangs) {
      gangs = gangs.where((gang) => gang.isNotEmpty).toList();
      if (gangs.isEmpty) return [];
      gangs.sort((a, b) => b.reduce((sum, element) => sum + element).compareTo(a.reduce((sum, element) => sum + element)));
      return gangs.expand((gang) => gang).toList();
    }
