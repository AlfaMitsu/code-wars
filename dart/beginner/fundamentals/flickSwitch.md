Flick Switch

    List<bool> flickSwitch(List<String> lst) {
      bool switchValue = true;
      return lst.map((e) {
        if (e == 'flick') {
          switchValue = !switchValue;
        }
        return switchValue;
      }).toList();
    }
