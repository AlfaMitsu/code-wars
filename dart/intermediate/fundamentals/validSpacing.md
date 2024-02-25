Valid Spacing

    bool valid_spacing(String text) {
      if (text.isEmpty) return true;
      
      return !text.startsWith(' ') && !text.endsWith(' ') && !text.contains('  ');
    }
