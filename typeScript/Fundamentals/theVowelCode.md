The Vowel Code

    export function encode(string: string): string {
      return string.replace(/[aeiou]/g, (match) => {
        switch (match) {
          case 'a': return '1';
          case 'e': return '2';
          case 'i': return '3';
          case 'o': return '4';
          case 'u': return '5';
          default: return match;
        }
      });
    }
    
    export function decode(string: string): string {
      return string.replace(/[12345]/g, (match) => {
        switch (match) {
          case '1': return 'a';
          case '2': return 'e';
          case '3': return 'i';
          case '4': return 'o';
          case '5': return 'u';
          default: return match;
        }
      });
    }
