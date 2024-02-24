Find the smallest Integer in the Array

    int findSmallestInt(List<int> arr) {
      return arr.reduce((value, element) => value < element ? value : element);
    }
