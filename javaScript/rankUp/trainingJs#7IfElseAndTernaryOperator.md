Training JS #7: if..else and ternary operator

    function saleHotdogs(n) {
      return n < 5 ? n * 100 : n < 10 ? n * 95 : n * 90;
    }
    
    console.log(saleHotdogs(4));  // Output: 400
    console.log(saleHotdogs(5));  // Output: 475
    console.log(saleHotdogs(9));  // Output: 855
    console.log(saleHotdogs(10)); // Output: 900
    console.log(saleHotdogs(15)); // Output: 1350
