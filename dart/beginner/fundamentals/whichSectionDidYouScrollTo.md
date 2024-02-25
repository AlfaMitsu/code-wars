Which section did you scroll to?

    int getSectionId(int n, List<int> a) {
      int totalHeight = 0;
      for (int i = 0; i < a.length; i++) {
        totalHeight += a[i];
        if (n < totalHeight) {
          return i;
        }
      }
      return -1;
    }
