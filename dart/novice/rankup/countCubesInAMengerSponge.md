Count Cubes in a Menger Sponge

    BigInt calcMs(int n) {
      BigInt result = BigInt.one;
      for (var i = 0; i < n; i++) {
        result *= BigInt.from(20);
      }
      return result;
    }
