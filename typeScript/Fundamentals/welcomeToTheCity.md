Welcom to the City

    export const sayHello = (name: string[], city: string, state: string): string => {
        const fullName = name.join(' ');
        return `Hello, ${fullName}! Welcome to ${city}, ${state}!`;
    };
