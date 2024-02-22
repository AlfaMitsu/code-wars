Disarium Number (Special Numbers Series #3)

    import 'dart:math';
    
    String disariumNumber(int n) {
      String numStr = n.toString();
      int sum = 0;
      for (int i = 0; i < numStr.length; i++) {
        sum += pow(int.parse(numStr[i]), i + 1) as int;
      }
      return sum == n ? "Disarium !!" : "Not !!";
    }
