Simple Pig Latin

    function pigIt(str){
      return str.replace(/(\w)(\w*)/g, (match, first, rest) => rest + first + 'ay');
    }
    
    // Examples
    console.log(pigIt('Pig latin is cool')); // igPay atinlay siay oolcay
    console.log(pigIt('Hello world !'));     // elloHay orldway !
