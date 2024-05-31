Training JS #29: methods of arrayObject---concat() and join()

    export function bigToSmall(arr: number[][]): string {
        const flatArr = arr.reduce((acc, val) => acc.concat(val), []);
        const sortedArr = flatArr.sort((a, b) => b - a);
        return sortedArr.join(">");
    }
