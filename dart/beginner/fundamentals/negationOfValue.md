Negation of Value

    bool negationValue(String str, bool val) {
      if (str.isEmpty) {
        return val;
      }
      return str.length % 2 == 0 ? val : !val;
    }
