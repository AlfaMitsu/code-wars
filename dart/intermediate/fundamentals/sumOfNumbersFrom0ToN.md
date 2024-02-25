Sum of numbers from 0 to N

    class SequenceSum{
      static String showSequence(int n)
      {
        if (n == 0) return "0=0";
        if (n < 0) return "$n<0";
    
        var sequence = List.generate(n + 1, (index) => index).join('+');
        var sum = (n * (n + 1)) ~/ 2;
        return '$sequence = $sum';
      }
    }
