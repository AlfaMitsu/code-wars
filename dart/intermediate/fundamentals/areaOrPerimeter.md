Area or Perimeter

    int area_or_perimeter(int l, int w) {
      if (l == w) {
        // Square: return area (side * side)
        return l * l;
      } else {
        // Rectangle: return perimeter (2 * (length + width))
        return 2 * (l + w);
      }
    }
