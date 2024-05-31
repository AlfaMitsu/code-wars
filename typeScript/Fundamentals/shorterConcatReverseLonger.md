Reverse Concat Reverse Longer

    export function shorterReverseLonger(a: string, b: string): string {
        if (a.length < b.length) {
            return a + b.split("").reverse().join("") + a;
        } else if (a.length > b.length) {
            return b + a.split("").reverse().join("") + b;
        } else {
            return b + a.split("").reverse().join("") + b;
        }
    }
