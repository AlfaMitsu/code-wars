Seats in theater

    int seatsInTheater(int nCols, int nRows, int col, int row) {
      int peopleToLeft = nCols - col + 1;
      int peopleBehind = nRows - row;
      return peopleToLeft * peopleBehind;
    }
