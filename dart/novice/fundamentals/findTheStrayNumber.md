Find the Stray Number

    int stray(List<int> numbers) {
      Map<int, int> countMap = {};
      for (int number in numbers) {
        if (countMap.containsKey(number)) {
          countMap[number] = countMap[number]! + 1;
        } else {
          countMap[number] = 1;
        }
      }
    
      for (int number in numbers) {
        if (countMap[number] == 1) {
          return number;
        }
      }
    
      return 0; // Default return value, should not be reached
    }
