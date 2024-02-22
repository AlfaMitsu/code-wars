Parts of a list

    List<List<String>> partlist(List<String> arr) {
      List<List<String>> result = [];
      for (int i = 1; i < arr.length; i++) {
        List<String> part1 = arr.sublist(0, i);
        List<String> part2 = arr.sublist(i);
        result.add([part1.join(' '), part2.join(' ')]);
      }
      return result;
    }
