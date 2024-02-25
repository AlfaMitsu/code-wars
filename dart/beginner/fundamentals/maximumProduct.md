Maximum Product

    int adjacentElementsProduct(List<int> array) {
      int maxProduct = array[0] * array[1];
      for (int i = 1; i < array.length - 1; i++) {
        int product = array[i] * array[i + 1];
        if (product > maxProduct) {
          maxProduct = product;
        }
      }
      return maxProduct;
    }
