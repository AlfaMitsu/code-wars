Array Ladders 3

    List<int> arrayLeaders(List<int> numbers) {
      List<int> result = [];
      
      for (int i = 0; i < numbers.length; i++) {
        int sum = 0;
        for (int j = i + 1; j < numbers.length; j++) {
          sum += numbers[j];
        }
        if (numbers[i] > sum) {
          result.add(numbers[i]);
        }
      }
      
      return result;
    }
