Fill the Hard Disk Drive

    int save(List<int> sizes, int hd) {
      int totalSize = 0;
      int count = 0;
    
      for (int size in sizes) {
        if (totalSize + size <= hd) {
          totalSize += size;
          count++;
        } else {
          break;
        }
      }
    
      return count;
    }
