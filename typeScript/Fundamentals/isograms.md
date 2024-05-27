Isograms

    export function isIsogram(str: string): boolean {
      const letters = str.toLowerCase().replace(/ /g, '').split('');
      const uniqueLetters = new Set(letters);
      return letters.length === uniqueLetters.size;
    }
