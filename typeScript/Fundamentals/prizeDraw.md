Prize Draw

    export function rank(st: string, we: number[], n: number): string {
        if (st === '') return 'No participants';
    
        const names = st.split(',');
        if (n > names.length) return 'Not enough participants';
    
        const charCodeA = 'A'.charCodeAt(0) - 1;
        const winningNumbers = names.map((name, index) => {
            const sum = name.toUpperCase().split('').reduce((acc, char) => acc + char.charCodeAt(0) - charCodeA, 0);
            return (sum + name.length) * we[index];
        });
    
        const sortedNames = names.slice().sort((a, b) => {
            const diff = winningNumbers[names.indexOf(b)] - winningNumbers[names.indexOf(a)];
            return diff === 0 ? a.localeCompare(b) : diff;
        });
    
        return sortedNames[n - 1];
    }
    
    // Test
    const names = "COLIN,AMANDBA,AMANDAB,CAROL,PauL,JOSEPH";
    const weights = [1, 4, 4, 5, 2, 1];
    const n = 4;
    console.log(rank(names, weights, n)); // Output: "PauL"
