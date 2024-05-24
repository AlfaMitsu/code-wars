Pick Peaks

    function pickPeaks(arr) {
      let pos = [];
      let peaks = [];
    
      for (let i = 1; i < arr.length - 1; i++) {
        if (arr[i] > arr[i - 1]) {
          let plateauStart = i;
          while (i < arr.length - 1 && arr[i] === arr[i + 1]) {
            i++;
          }
          if (i < arr.length - 1 && arr[i] > arr[i + 1]) {
            pos.push(plateauStart);
            peaks.push(arr[plateauStart]);
          }
        }
      }
    
      return { pos, peaks };
    }
    
    // Example usage
    console.log(pickPeaks([3, 2, 3, 6, 4, 1, 2, 3, 2, 1, 2, 3])); // { pos: [ 3, 7 ], peaks: [ 6, 3 ] }
    console.log(pickPeaks([1, 2, 2, 2, 1])); // { pos: [ 1 ], peaks: [ 2 ] }
