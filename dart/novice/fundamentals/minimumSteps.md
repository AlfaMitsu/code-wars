Minimum Steps

    int minimumSteps(List<int> nums, int value) {
      nums.sort();
      int sum = 0;
      int count = 0;
      for (int i = 0; i < nums.length; i++) {
        if (sum >= value) {
          break;
        }
        sum += nums[i];
        count++;
      }
      return count - 1; // Subtract 1 because the last number is added but sum is already >= value
    }
