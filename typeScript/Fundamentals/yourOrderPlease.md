Your order please

    export function order(words: string): string {
        if (!words) {
            return "";
        }
    
        return words
            .split(" ")
            .sort((a, b) => {
                const matchA = a.match(/\d+/);
                const matchB = b.match(/\d+/);
                const numA = matchA ? parseInt(matchA[0]) : 0;
                const numB = matchB ? parseInt(matchB[0]) : 0;
                return numA - numB;
            })
            .join(" ");
    }
