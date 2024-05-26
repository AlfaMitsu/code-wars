Scramblies

    export function scramble(str1: string, str2: string): boolean {
        const charCounts: Record<string, number> = {};
    
        for (const char of str1) {
            charCounts[char] = (charCounts[char] || 0) + 1;
        }
    
        for (const char of str2) {
            if (!charCounts[char]) {
                return false;
            }
            charCounts[char]--;
        }
    
        return true;
    }
