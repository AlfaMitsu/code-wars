Base64 Encoding

    export function toBase64(str: string): string {
        return Buffer.from(str, 'utf-8').toString('base64').replace(/=/g, '');
    }
    
    export function fromBase64(str: string): string {
        return Buffer.from(str, 'base64').toString('utf-8');
    }
