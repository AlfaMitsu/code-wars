Banker's Plan

    bool fortune(int f0, double p, int c0, int n, double i) {
      double balance = f0.toDouble();
      double inflation = i / 100.0;
      double interest = p / 100.0;
      
      for (int year = 1; year <= n; year++) {
        double withdrawal = balance >= c0.toDouble() ? c0.toDouble() : balance;
        balance -= withdrawal;
        double interestAmount = balance * interest;
        balance += interestAmount;
        balance -= c0.toDouble();
        c0 += (c0.toDouble() * inflation).toInt();
        
        if (balance < 0) {
          return false;
        }
      }
      
      return true;
    }
