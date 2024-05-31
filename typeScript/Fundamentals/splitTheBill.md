Split the Bill

    export function splitTheBill(x: {[k: string]: number}): {[k: string]: number} {
        const names = Object.keys(x);
        const total = names.reduce((acc, name) => acc + x[name], 0);
        const average = total / names.length;
    
        const result: {[k: string]: number} = {};
    
        names.forEach(name => {
            result[name] = Math.round((x[name] - average) * 100) / 100;
        });
    
        return result;
    }
