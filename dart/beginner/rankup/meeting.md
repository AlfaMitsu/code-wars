Meeting

    String meeting(String s) {
      // Split the input string into individual guest strings
      List<String> guests = s.split(';');
    
      // Convert each guest string to uppercase and split into first name and last name
      List<List<String>> formattedGuests = guests.map((guest) {
        List<String> names = guest.split(':');
        return [names[1].toUpperCase(), names[0].toUpperCase()];
      }).toList();
    
      // Sort the formatted guests by last name, then first name
      formattedGuests.sort((a, b) {
        if (a[0] == b[0]) {
          return a[1].compareTo(b[1]);
        }
        return a[0].compareTo(b[0]);
      });
    
      // Join the sorted and formatted guest names
      return formattedGuests.map((guest) => '(${guest[0]}, ${guest[1]})').join('');
    }
