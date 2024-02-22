Help the Bookseller

    String stockSummary(List<String> lstOfArt, List<String> lstOf1stLetter) {
      if (lstOfArt.isEmpty || lstOf1stLetter.isEmpty) return "";
    
      Map<String, int> categoryQuantities = {};
      lstOfArt.forEach((book) {
        String category = book.split(" ")[0][0];
        int quantity = int.parse(book.split(" ")[1]);
        categoryQuantities[category] = (categoryQuantities[category] ?? 0) + quantity;
      });
    
      return lstOf1stLetter
          .map((category) => "($category : ${categoryQuantities[category] ?? 0})")
          .join(" - ");
    }
