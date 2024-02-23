Moves in squared strings

    String vertMirror(String strng) {
      return strng.split('\n').map((line) => line.split('').reversed.join()).join('\n');
    }
    
    String horMirror(String strng) {
      return strng.split('\n').reversed.join('\n');
    }
    
    String oper(String Function(String) func, String s) {
      return func(s);
    }
