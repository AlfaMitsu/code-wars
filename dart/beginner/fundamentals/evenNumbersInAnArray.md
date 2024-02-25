Even numbers in an array

    List<int> evenNumbers(List<int> arr, int n) {
      List<int> result = [];
      for (int i = arr.length - 1; i >= 0 && result.length < n; i--) {
        if (arr[i] % 2 == 0) {
          result.add(arr[i]);
        }
      }
      return result.reversed.toList();
    }
