Histogram

    String histogram(List<int> results) {
      String hist = '';
      for (int i = 6; i >= 1; i--) {
        String line = '$i|';
        int count = results[i - 1];
        line += count > 0 ? '#' * count + ' $count' : '';
        hist += '$line\n';
      }
      return hist;
    }
