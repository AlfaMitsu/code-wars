Find out whether the shape is a cube

    export function cubeChecker(volume: number, side: number): boolean {
        if (volume <= 0 || side <= 0) {
            return false;
        }
    
        const calculatedSideLength = Math.cbrt(volume);
    
        return Math.abs(side - calculatedSideLength) < Number.EPSILON;
    }
