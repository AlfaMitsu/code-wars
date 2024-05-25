Simple Encryption #1 - Alternating Split

    function encrypt(text, n) {
      if (!text || n <= 0) return text;
      
      let encryptedText = text;
      for (let i = 0; i < n; i++) {
        let oddChars = "";
        let evenChars = "";
        for (let j = 0; j < encryptedText.length; j++) {
          if (j % 2 === 1) {
            oddChars += encryptedText[j];
          } else {
            evenChars += encryptedText[j];
          }
        }
        encryptedText = oddChars + evenChars;
      }
      
      return encryptedText;
    }
    
    function decrypt(encryptedText, n) {
      if (!encryptedText || n <= 0) return encryptedText;
      
      const midpoint = Math.floor(encryptedText.length / 2);
      let decryptedText = encryptedText;
      for (let i = 0; i < n; i++) {
        let text = "";
        for (let j = 0; j < midpoint; j++) {
          text += decryptedText[midpoint + j] + decryptedText[j];
        }
        if (encryptedText.length % 2 !== 0) {
          text += decryptedText[encryptedText.length - 1];
        }
        decryptedText = text;
      }
      
      return decryptedText;
    }
    
    // Example usage
    console.log(encrypt("012345", 1));  // "135024"
    console.log(encrypt("012345", 2));  // "304152"
    console.log(encrypt("012345", 3));  // "012345"
    
    console.log(decrypt("135024", 1));  // "012345"
    console.log(decrypt("304152", 2));  // "012345"
    console.log(decrypt("012345", 3));  // "012345"
