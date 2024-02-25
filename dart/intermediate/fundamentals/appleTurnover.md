Apple Turnover

    String apple(dynamic a) {
      int num = a is String ? int.parse(a) : a;
      return num * num > 1000 ? "It's hotter than the sun!!" : "Help yourself to a honeycomb Yorkie for the glovebox.";
    }
