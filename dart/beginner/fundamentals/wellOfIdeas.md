Well of Ideas - Easy

    String well(List<String> x) {
      int goodIdeas = x.where((idea) => idea == 'good').length;
      if (goodIdeas == 0) {
        return 'Fail!';
      } else if (goodIdeas <= 2) {
        return 'Publish!';
      } else {
        return 'I smell a series!';
      }
    }
