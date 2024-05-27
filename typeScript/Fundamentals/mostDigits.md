Most Digits

    export class Kata {
      static findLongest(array: number[]): number {
        return array.reduce((acc, curr) => {
          return String(curr).length > String(acc).length ? curr : acc;
        });
      }
    }
