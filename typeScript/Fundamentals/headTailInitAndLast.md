Head Tail Init and Last

    export const head = (arr: any[]): any => arr[0];
    
    export const tail = (arr: any[]): any[] => arr.slice(1);
    
    export const init = (arr: any[]): any[] => arr.slice(0, -1);
    
    export const last = (arr: any[]): any => arr[arr.length - 1];
    
    // Test
    console.log(head([1, 2, 3, 4, 5])); // Output: 1
    console.log(tail([1, 2, 3, 4, 5])); // Output: [2, 3, 4, 5]
    console.log(init([1, 2, 3, 4, 5])); // Output: [1, 2, 3, 4]
    console.log(last([1, 2, 3, 4, 5])); // Output: 5
