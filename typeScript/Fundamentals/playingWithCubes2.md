Playing with Cubes 2

    export class Cube {
      
      private _side: number = 0;
    
      constructor(side: number = 0) {
        this.setSide(side);
      }
    
      public getSide(): number {
        return this._side;
      }
    
      public setSide(value: number) {
        this._side = Math.abs(value);
      }
    }
