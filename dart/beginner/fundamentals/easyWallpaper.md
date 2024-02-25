Easy Wallpaper

    String wallpaper(double l, double w, double h) {
      List<String> numbers = ["zero", "one", "two", "three", "four", "five", "six", "seven", "eight", "nine", "ten", "eleven", "twelve", "thirteen", "fourteen", "fifteen", "sixteen", "seventeen", "eighteen", "nineteen", "twenty"];
    
      if (l == 0 || w == 0 || h == 0) {
        return "zero";
      }
    
      double rollLength = 10.0;
      double rollWidth = 0.52;
      double extraPercent = 0.15;
      double totalArea = 2 * (l + w) * h;
      double extraArea = totalArea * extraPercent;
      double totalWallpaperArea = totalArea + extraArea;
      double rolls = totalWallpaperArea / (rollLength * rollWidth);
    
      return numbers[rolls.ceil().toInt()];
    }
