Rot13

function rot13(message) {
  return message.split('').map(char => {
    if (char.match(/[a-z]/i)) {
      const code = char.charCodeAt(0);
      let shiftedCode;

      if (code >= 65 && code <= 90) { // Uppercase letters
        shiftedCode = ((code - 65 + 13) % 26) + 65;
      } else if (code >= 97 && code <= 122) { // Lowercase letters
        shiftedCode = ((code - 97 + 13) % 26) + 97;
      }

      return String.fromCharCode(shiftedCode);
    }

    return char; // Non-letter characters remain unchanged
  }).join('');
}

// Example usage:
console.log(rot13("Hello, World!")); // Outputs: Uryyb, Jbeyq!
console.log(rot13("Uryyb, Jbeyq!")); // Outputs: Hello, World!
