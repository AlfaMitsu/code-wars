esreveR

    reverse = function(array) {
      for (let i = 0; i < Math.floor(array.length / 2); i++) {
        const temp = array[i];
        array[i] = array[array.length - 1 - i];
        array[array.length - 1 - i] = temp;
      }
      return array;
    };
