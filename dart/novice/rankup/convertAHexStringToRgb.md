Convert a Hex String to RGB

    Map<String, int> hexToRGB(String hex) {
      hex = hex.replaceAll("#", "");
      int hexValue = int.parse(hex, radix: 16);
      int r = (hexValue >> 16) & 0xFF;
      int g = (hexValue >> 8) & 0xFF;
      int b = hexValue & 0xFF;
      return {"r": r, "g": g, "b": b};
    }
