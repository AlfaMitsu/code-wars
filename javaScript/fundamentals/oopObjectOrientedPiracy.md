OOP: Object Oriented Piracy

    class Ship {
      constructor(draft, crew) {
        this.draft = draft;
        this.crew = crew;
      }
    
      isWorthIt() {
        return (this.draft - this.crew * 1.5) > 20;
      }
    }
    
    // Example usage
    const titanic = new Ship(15, 10);
    console.log(titanic.isWorthIt()); // Output: false
