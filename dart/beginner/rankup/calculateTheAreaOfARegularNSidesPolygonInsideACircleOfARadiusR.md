Calculate the area of a regular n sides polygon inside a circle of radius r


    import 'dart:math' as math;
    
    double areaOfPolygonInsideCircle(double r, int n) {
      double sideLength = 2 * r * math.sin(math.pi / n);
      double apothem = r * math.cos(math.pi / n);
      double area = 0.5 * n * sideLength * apothem;
      return double.parse((area).toStringAsFixed(3));
    }
