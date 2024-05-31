Hello, Name or World!

    function hello(name) {
      if (name && name.trim() !== "") {
        name = name.charAt(0).toUpperCase() + name.slice(1).toLowerCase();
        return "Hello, " + name + "!";
      } else {
        return "Hello, World!";
      }
    }
