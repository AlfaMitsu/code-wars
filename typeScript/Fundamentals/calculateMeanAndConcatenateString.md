Calculate Mean and Concatenate String

    export function mean(lst: string[]): [number, string] {
      // Extract integers
      const integers = lst.filter(item => !isNaN(parseInt(item)));
    
      // Calculate mean
      const sum = integers.reduce((acc, curr) => acc + parseInt(curr), 0);
      const mean = sum / 10;
    
      // Concatenate characters
      const characters = lst.filter(item => isNaN(parseInt(item))).join('');
    
      return [mean, characters];
    }
