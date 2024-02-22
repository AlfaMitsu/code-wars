Largest 5 digit number in a series

    int solution(String digits) {
      int greatest = 0;
      for (int i = 0; i <= digits.length - 5; i++) {
        int sequence = int.parse(digits.substring(i, i + 5));
        if (sequence > greatest) {
          greatest = sequence;
        }
      }
      return greatest;
    }
