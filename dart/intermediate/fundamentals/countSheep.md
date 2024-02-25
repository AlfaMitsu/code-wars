Count Sheep

    String countSheep(int numb) {
      String result = "";
      for (int i = 1; i <= numb; i++) {
        result += "$i sheep...";
      }
      return result;
    }
