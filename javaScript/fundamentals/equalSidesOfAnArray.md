Equal sides of an array

    function findEvenIndex(arr) {
        for (let i = 0; i < arr.length; i++) {
            let leftSum = arr.slice(0, i).reduce((acc, curr) => acc + curr, 0);
            let rightSum = arr.slice(i + 1).reduce((acc, curr) => acc + curr, 0);
            if (leftSum === rightSum) {
                return i;
            }
        }
        return -1;
    }
