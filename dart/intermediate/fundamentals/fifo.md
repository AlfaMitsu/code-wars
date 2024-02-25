Page replacement algorithms: FIFO

    List<int> fifo(int n, List<int> referenceList) {
      List<int> memory = [];
      int oldestIndex = 0;
      for (int page in referenceList) {
        if (!memory.contains(page)) {
          if (memory.length < n) {
            memory.add(page);
          } else {
            memory[oldestIndex] = page;
            oldestIndex = (oldestIndex + 1) % n;
          }
        }
      }
      while (memory.length < n) {
        memory.add(-1);
      }
      return memory;
    }
