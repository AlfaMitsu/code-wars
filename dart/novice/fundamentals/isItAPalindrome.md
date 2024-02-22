Is it a Palindrome?

    bool isPalindrome(String str) {
      String reversed = str.toLowerCase().split('').reversed.join('');
      return str.toLowerCase() == reversed;
    }
