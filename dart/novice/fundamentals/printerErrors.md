Printer Errors

    String printerError(String s) {
      int errorCount = s.split('').where((char) => char.codeUnitAt(0) > 'm'.codeUnitAt(0)).length;
      return '$errorCount/${s.length}';
    }
