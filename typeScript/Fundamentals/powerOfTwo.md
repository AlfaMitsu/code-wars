Power of Two

    export function isPowerOfTwo(n: number): boolean {
        return n > 0 && (n & (n - 1)) === 0;
    }
    
    // Test
    console.log(isPowerOfTwo(1024)); // Output: true
    console.log(isPowerOfTwo(4096)); // Output: true
    console.log(isPowerOfTwo(333));  // Output: false
