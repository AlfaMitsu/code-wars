You're a square!

    import 'dart:math';
    
    bool isSquare(int n) {
      if (n < 0) return false;
      int sqrtN = sqrt(n).toInt();
      return sqrtN * sqrtN == n;
    }
