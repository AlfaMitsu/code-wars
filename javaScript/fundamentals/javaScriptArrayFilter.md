JavaScript Array Filter

    function getEvenNumbers(numbersArray){
      return numbersArray.filter(function(number) {
        return number % 2 === 0;
      });
    }
    
    // Example usage:
    console.log(getEvenNumbers([2, 4, 5, 6])); // [2, 4, 6]
    console.log(getEvenNumbers([1, 3, 5, 7])); // []
    console.log(getEvenNumbers([10, 15, 20, 25])); // [10, 20]
