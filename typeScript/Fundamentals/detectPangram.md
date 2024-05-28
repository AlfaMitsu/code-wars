Detect Pangram

    export const isPangram = (phrase: string): boolean => {
        const alphabet = 'abcdefghijklmnopqrstuvwxyz';
        const letters = new Set(phrase.toLowerCase().replace(/[^a-z]/g, ''));
        return alphabet.split('').every(letter => letters.has(letter));
    }
    
    // Test
    console.log(isPangram("The quick brown fox jumps over the lazy dog")); // Output: true
    console.log(isPangram("Hello, world!")); // Output: false
