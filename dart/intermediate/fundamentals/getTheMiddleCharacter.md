Get the Middle character

    String getMiddle(String s) {
      int length = s.length;
      int midIndex = length ~/ 2;
      return length.isOdd ? s[midIndex] : s.substring(midIndex - 1, midIndex + 1);
    }
