ROT13

    export function rot13(str: string): string {
        return str.replace(/[A-Za-z]/g, (char) => {
            const charCode = char.charCodeAt(0);
            let offset = 13;
    
            if (char >= 'a' && char <= 'z') {
                offset = 97;
            } else if (char >= 'A' && char <= 'Z') {
                offset = 65;
            }
    
            return String.fromCharCode(((charCode - offset + 13) % 26) + offset);
        });
    }
