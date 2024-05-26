Fold an Array

    export function foldArray(array: number[], runs: number): number[] {
        let result = array.slice(); // Create a copy of the original array
    
        for (let i = 0; i < runs; i++) {
            const folded = [];
            const length = result.length;
            const mid = Math.floor(length / 2);
    
            for (let j = 0; j < mid; j++) {
                folded.push(result[j] + result[length - 1 - j]);
            }
    
            if (length % 2 !== 0) {
                folded.push(result[mid]);
            }
    
            result = folded;
        }
    
        return result;
    }
