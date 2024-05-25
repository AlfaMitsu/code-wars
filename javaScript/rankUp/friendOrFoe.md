Friend or Foe?

    function friend(friends) {
      return friends.filter(name => name.length === 4);
    }
    
    // Test case
    let input = ["Ryan", "Kieran", "Jason", "Yous"];
    console.log(friend(input)); // Output: ["Ryan", "Yous"]
