Sum of Pairs

    export function sumPairs(ints: number[], s: number): [number, number] | void {
        const seenNumbers = new Set<number>();
    
        for (let i = 0; i < ints.length; i++) {
            const complement = s - ints[i];
            if (seenNumbers.has(complement)) {
                return [complement, ints[i]];
            }
            seenNumbers.add(ints[i]);
        }
    
        return undefined;
    }
