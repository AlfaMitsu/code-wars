Buying a car

    function nbMonths(startPriceOld, startPriceNew, savingPerMonth, percentLossByMonth) {
      let months = 0;
      let savings = 0;
      let oldCarPrice = startPriceOld;
      let newCarPrice = startPriceNew;
      let percentLoss = percentLossByMonth;
    
      while (oldCarPrice + savings < newCarPrice) {
        months++;
        
        // Increase savings
        savings += savingPerMonth;
        
        // Update the prices of the cars
        if (months % 2 === 0) {
          percentLoss += 0.5;
        }
        oldCarPrice -= oldCarPrice * (percentLoss / 100);
        newCarPrice -= newCarPrice * (percentLoss / 100);
      }
    
      let remainingMoney = Math.round(oldCarPrice + savings - newCarPrice);
      return [months, remainingMoney];
    }
    
    // Example usage:
    console.log(nbMonths(2000, 8000, 1000, 1.5)); // [6, 766]
    console.log(nbMonths(12000, 8000, 1000, 1.5)); // [0, 4000]
    console.log(nbMonths(8000, 8000, 1000, 1.5)); // [0, 0]
