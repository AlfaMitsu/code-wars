Exes and Ohs

    bool XO(String str) {
      var lowerCaseStr = str.toLowerCase();
      var xCount = lowerCaseStr.split('x').length - 1;
      var oCount = lowerCaseStr.split('o').length - 1;
      return xCount == oCount;
    }
