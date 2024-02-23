Find the Parity Outlier

    int find(List<int> integers) {
      bool isEven(int n) => n % 2 == 0;
      
      int oddCount = 0;
      int evenCount = 0;
      int oddIndex = 0;
      int evenIndex = 0;
      
      for (int i = 0; i < integers.length; i++) {
        if (isEven(integers[i])) {
          evenCount++;
          evenIndex = i;
        } else {
          oddCount++;
          oddIndex = i;
        }
      }
      
      return (evenCount == 1) ? integers[evenIndex] : integers[oddIndex];
    }
