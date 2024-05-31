Check the exam

    function checkExam(array1, array2) {
        let score = 0;
        for (let i = 0; i < array1.length; i++) {
            if (array2[i] === "") {
                // No answer given
                score += 0;
            } else if (array1[i] === array2[i]) {
                // Correct answer
                score += 4;
            } else {
                // Incorrect answer
                score -= 1;
            }
        }
        // Ensure score is not negative
        return Math.max(score, 0);
    }
