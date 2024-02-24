Valid Braces

    bool validBraces(String braces) {
      final stack = <String>[];
      final matches = {
        ')': '(',
        ']': '[',
        '}': '{',
      };
    
      for (var brace in braces.split('')) {
        if (matches.containsValue(brace)) {
          stack.add(brace);
        } else if (matches.containsKey(brace)) {
          if (stack.isEmpty || stack.last != matches[brace]) {
            return false;
          }
          stack.removeLast();
        }
      }
    
      return stack.isEmpty;
    }
