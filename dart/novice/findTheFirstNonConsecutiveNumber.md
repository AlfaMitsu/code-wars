Find the first non-consecutive number

    int? findFirstNonConsecutive(List<int> numbers) {
      for (int i = 1; i < numbers.length; i++) {
        if (numbers[i] != numbers[i - 1] + 1) {
          return numbers[i];
        }
      }
      return null;
    }

    void main() {
      test("a simple example", () {
        List<int> numbers = [1, 2, 3, 4, 6, 7, 8];
        int? result = findFirstNonConsecutive(numbers);
        print("First non-consecutive number: $result");
      });
    }
