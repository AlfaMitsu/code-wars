Counting Change Combinations

    function countChange(money, coins) {
      let ways = new Array(money + 1).fill(0);
      ways[0] = 1;
    
      for (let coin of coins) {
        for (let i = coin; i <= money; i++) {
          ways[i] += ways[i - coin];
        }
      }
    
      return ways[money];
    }
    
    // Test cases
    console.log(countChange(4, [1, 2]));   // Output: 3
    console.log(countChange(10, [5, 2, 3]));   // Output: 4
    console.log(countChange(11, [5, 7]));   // Output: 0
