Testing 1-2-3

    var number = function(array) {
      return array.map((line, index) => `${index + 1}: ${line}`);
    }
    
    // Test examples
    console.log(number([])); // []
    console.log(number(["a", "b", "c"])); // ["1: a", "2: b", "3: c"]
    console.log(number(["Hello", "world", "this", "is", "a", "test"])); // ["1: Hello", "2: world", "3: this", "4: is", "5: a", "6: test"]
