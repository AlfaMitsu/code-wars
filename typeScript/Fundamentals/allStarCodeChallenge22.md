All Star Code Challenge #22

    export function toTime(seconds: number): string {
        const hours = Math.floor(seconds / 3600);
        const minutes = Math.floor((seconds % 3600) / 60);
        return `${hours} hour(s) and ${minutes} minute(s)`;
    }
    
    // Test
    console.log(toTime(3600)); // Output: "1 hour(s) and 0 minute(s)"
    console.log(toTime(3601)); // Output: "1 hour(s) and 0 minute(s)"
    console.log(toTime(3500)); // Output: "0 hour(s) and 58 minute(s)"
    console.log(toTime(323500)); // Output: "89 hour(s) and 51 minute(s)"
