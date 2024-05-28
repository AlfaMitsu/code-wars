Parse Float

    export function parseF(s: string): number | null {
        const result = parseFloat(s);
        return isNaN(result) ? null : result;
    }
    
    // Test
    console.log(parseF("3.14")); // Output: 3.14
    console.log(parseF("Hello")); // Output: null
