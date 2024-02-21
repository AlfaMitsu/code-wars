Create Phone Number

    String createPhoneNumber(List<int> numbers) {
      String firstPart = numbers.sublist(0, 3).join('');
      String secondPart = numbers.sublist(3, 6).join('');
      String thirdPart = numbers.sublist(6, 10).join('');
      return '($firstPart) $secondPart-$thirdPart';
    }
