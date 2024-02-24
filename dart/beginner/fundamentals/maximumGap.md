Maximum Gap

    int maxGap(List<int> nums) {
      nums.sort();
      int maxDifference = 0;
      for (int i = 1; i < nums.length; i++) {
        int difference = (nums[i] - nums[i - 1]).abs();
        if (difference > maxDifference) {
          maxDifference = difference;
        }
      }
      return maxDifference;
    }
