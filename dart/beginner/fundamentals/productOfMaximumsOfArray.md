Product Of Maximums Of Array

    int maxProduct(List<int> arr, int size) {
      arr.sort((a, b) => b.compareTo(a));
      int product = 1;
      for (int i = 0; i < size; i++) {
        product *= arr[i];
      }
      return product;
    }
