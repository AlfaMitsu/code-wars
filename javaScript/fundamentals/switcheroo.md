Switcheroo

    function switcheroo(x) {
      return x.replace(/[ab]/g, function(match) {
        return match === 'a' ? 'b' : 'a';
      });
    }
    
    // Example usage:
    console.log(switcheroo('acb')); // 'bca'
    console.log(switcheroo('aabacbaa')); // 'bbabcabb'
