Product Array

    List<int> productArray(List<int> nums) {
      List<int> result = List.filled(nums.length, 1);
      
      int product = 1;
      for (int i = 0; i < nums.length; i++) {
        result[i] *= product;
        product *= nums[i];
      }
    
      product = 1;
      for (int i = nums.length - 1; i >= 0; i--) {
        result[i] *= product;
        product *= nums[i];
      }
    
      return result;
    }
