RGB to Hex Conversion

    String rgb(int r, int g, int b) {
      // Ensure values are within the valid range
      r = r.clamp(0, 255);
      g = g.clamp(0, 255);
      b = b.clamp(0, 255);
    
      // Convert decimal values to hexadecimal
      String hexR = r.toRadixString(16).padLeft(2, '0');
      String hexG = g.toRadixString(16).padLeft(2, '0');
      String hexB = b.toRadixString(16).padLeft(2, '0');
    
      return '$hexR$hexG$hexB'.toUpperCase();
    }
