Anagram Detection

    var isAnagram = function(test, original) {
      const normalize = str => str.toLowerCase().split('').sort().join('');
      return normalize(test) === normalize(original);
    };
    
    // Test cases
    console.log(isAnagram("foefet", "toffee"));       // true
    console.log(isAnagram("Buckethead", "DeathCubeK"));// true
    console.log(isAnagram("hello", "world"));         // false
