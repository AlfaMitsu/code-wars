Odd or Even

    String oddOrEven(List<int> arr) {
      int sum = arr.isEmpty ? 0 : arr.reduce((a, b) => a + b);
      return sum % 2 == 0 ? "even" : "odd";
    }
