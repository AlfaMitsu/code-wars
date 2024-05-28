Parse Nice Int from Char Problem

    export function get_age(age: string): number {
        return parseInt(age[0]);
    }
    
    // Test
    console.log(get_age("1 year old")); // Output: 1
    console.log(get_age("5 years old")); // Output: 5
