Word a10n (Abbreviation)

    export function abbreviate(str: string): string {
        return str.split(/([a-zA-Z]+)/)
            .map(word => {
                if (/[a-zA-Z]{4,}/.test(word)) {
                    const first = word.charAt(0);
                    const last = word.charAt(word.length - 1);
                    const middle = word.length - 2;
                    return `${first}${middle}${last}`;
                }
                return word;
            })
            .join('');
    }
    
    // Test
    console.log(abbreviate("elephant-rides are really fun!"));
    // Output: "e6t-r3s are r4y fun!"
