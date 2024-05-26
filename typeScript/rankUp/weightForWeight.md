Weight for weight

    export function orderWeight(strng: string): string {
        const weights = strng.trim().split(/\s+/);
    
        function weightSum(num: string): number {
            return num.split('').reduce((sum, digit) => sum + parseInt(digit), 0);
        }
    
        weights.sort((a, b) => {
            const weightDiff = weightSum(a) - weightSum(b);
            if (weightDiff === 0) {
                return a.localeCompare(b);
            }
            return weightDiff;
        });
    
        return weights.join(' ');
    }
