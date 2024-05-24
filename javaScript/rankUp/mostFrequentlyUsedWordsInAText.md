Most Frequently used words in a text

    function topThreeWords(text) {
        let wordCount = new Map();
        text.toLowerCase().replace(/[A-Za-z]+('[A-Za-z]+)?/g, (word) => {
            wordCount.set(word, (wordCount.get(word) || 0) + 1);
        });
    
        let sortedWords = Array.from(wordCount.keys()).sort((a, b) => wordCount.get(b) - wordCount.get(a));
        return sortedWords.slice(0, 3);
    }
    
    // Example usage
    console.log(topThreeWords("In a village of La Mancha, the name of which I have no desire to call to mind, there lived not long since one of those gentlemen that keep a lance in the lance-rack, an old buckler, a lean hack, and a greyhound for coursing. An olla of rather more beef than mutton, a salad on most nights, scraps on Saturdays, lentils on Fridays, and a pigeon or so extra on Sundays, made away with three-quarters of his income."));
