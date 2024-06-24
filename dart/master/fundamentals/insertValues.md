Insert Values

    List<int> invert(List<int> arr) {
      // Create a new list with the additive inverses of the input list
      return arr.map((num) => -num).toList();
    }
    
    void main() {
      print(invert([1, 2, 3, 4, 5]));    // Output: [-1, -2, -3, -4, -5]
      print(invert([1, -2, 3, -4, 5]));  // Output: [-1, 2, -3, 4, -5]
      print(invert([]));                 // Output: []
    }
