Fake Binary

    export const fakeBin = (x:string):string => {
      return x.split('').map(digit => parseInt(digit) >= 5 ? '1' : '0').join('');
    };
