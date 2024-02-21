Difference of Volumes of Cuboids

    int findDifference(List<int> a, List<int> b) => (a.reduce((value, element) => value * element) - b.reduce((value, element) => value * element)).abs();
