Square every digit

    export class Kata {
      static squareDigits(num: number): number {
        const numStr = num.toString();
        let result = '';
        for (let i = 0; i < numStr.length; i++) {
          const digit = parseInt(numStr[i]);
          result += (digit * digit).toString();
        }
        return parseInt(result);
      }
    }
    
    // Test
    console.log(Kata.squareDigits(9119)); // Output: 811181
    console.log(Kata.squareDigits(765)); // Output: 493625
