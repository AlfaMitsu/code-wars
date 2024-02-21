Sum of Intervals

    int sumOfIntervals(List<List<int>> intervals) {
      intervals.sort((a, b) => a[0].compareTo(b[0]));
    
      int totalLength = 0;
      int currentStart = intervals[0][0];
      int currentEnd = intervals[0][1];
    
      for (int i = 1; i < intervals.length; i++) {
        if (intervals[i][0] <= currentEnd) {
          currentEnd = currentEnd > intervals[i][1] ? currentEnd : intervals[i][1];
        } else {
          totalLength += currentEnd - currentStart;
          currentStart = intervals[i][0];
          currentEnd = intervals[i][1];
        }
      }
    
      totalLength += currentEnd - currentStart;
    
      return totalLength;
    }
