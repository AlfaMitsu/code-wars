Find the smallest

    export function smallest(n: number): [number, number, number] {
        const numStr = String(n);
        let smallestNum = n;
        let smallestI = 0;
        let smallestJ = 0;
    
        for (let i = 0; i < numStr.length; i++) {
            for (let j = 0; j <= numStr.length; j++) {
                const removedDigit = numStr.slice(0, i) + numStr.slice(i + 1, numStr.length);
                const newNum = Number(removedDigit.slice(0, j) + numStr[i] + removedDigit.slice(j, removedDigit.length));
    
                if (newNum < smallestNum) {
                    smallestNum = newNum;
                    smallestI = i;
                    smallestJ = j;
                }
            }
        }
    
        return [smallestNum, smallestI, smallestJ];
    }
