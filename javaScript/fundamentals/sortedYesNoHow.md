Sorted? Yes? No? How?

    function isSortedAndHow(array) {
        let ascending = array.slice().sort((a, b) => a - b);
        let descending = array.slice().sort((a, b) => b - a);
    
        if (array.every((value, index) => value === ascending[index])) {
            return "yes, ascending";
        } else if (array.every((value, index) => value === descending[index])) {
            return "yes, descending";
        } else {
            return "no";
        }
    }
