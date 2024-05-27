Holiday VIII - Duty Free

    export function dutyFree(normPrice: number, discount: number, hol: number): number{
      const savingsPerBottle = normPrice * (discount / 100);
      const bottlesNeeded = hol / savingsPerBottle;
      return Math.floor(bottlesNeeded);
    }
