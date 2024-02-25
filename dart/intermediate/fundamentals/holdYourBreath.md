Hold your breath

    bool divingMinigame(List<int> lst) {
      int breath = 10;
      for (int altitude in lst) {
        if (altitude < 0) {
          breath -= 2;
        } else {
          breath = (breath + 4).clamp(0, 10);
        }
        if (breath <= 0) {
          return false;
        }
      }
      return true;
    }
