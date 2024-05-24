Whats the real floor

    function getRealFloor(n) {
      if (n > 13) {
        return n - 2;
      } else if (n > 0) {
        return n - 1;
      } else {
        return n;
      }
    }
    
    // Examples
    console.log(getRealFloor(1));  // 0
    console.log(getRealFloor(0));  // 0
    console.log(getRealFloor(5));  // 4
    console.log(getRealFloor(15)); // 13
    console.log(getRealFloor(-3)); // -3
