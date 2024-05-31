Delete occurrences of an element if it occurs more than n times

    function deleteNth(arr, n) {
        let count = {};
        return arr.filter(num => {
            count[num] = (count[num] || 0) + 1;
            return count[num] <= n;
        });
    }
