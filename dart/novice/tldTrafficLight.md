###Thinkful - Logic Drills: Traffic light

    String updateLight(String current) {
      switch (current) {
        case "green":
          return "yellow";
        case "yellow":
          return "red";
        case "red":
          return "green";
        default:
          return "invalid state";
      }
    }
