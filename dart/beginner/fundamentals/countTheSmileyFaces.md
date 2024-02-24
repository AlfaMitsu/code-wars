Count the smiley faces

    int countSmileys(List<String> arr) {
      final pattern = RegExp(r"[:;][-~]?[)D]");
      return arr.where((face) => pattern.hasMatch(face)).length;
    }
