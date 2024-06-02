Two Fighters, One Winner

    function declareWinner(fighter1, fighter2, firstAttacker) {
      // Determine who attacks first
      let attacker = firstAttacker === fighter1.name ? fighter1 : fighter2;
      let defender = firstAttacker === fighter1.name ? fighter2 : fighter1;
    
      while (fighter1.health > 0 && fighter2.health > 0) {
        // Attacker attacks defender
        defender.health -= attacker.damagePerAttack;
        
        // Swap roles
        if (defender.health > 0) {
          [attacker, defender] = [defender, attacker];
        }
      }
    
      // Return the name of the winner
      return attacker.health > 0 ? attacker.name : defender.name;
    }
    
    // Fighter class definition
    function Fighter(name, health, damagePerAttack) {
      this.name = name;
      this.health = health;
      this.damagePerAttack = damagePerAttack;
      this.toString = function() {
        return this.name;
      }
    }
