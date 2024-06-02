Closest pair of points in linearithmic time

    function closestPair(points) {
      if (points.length < 2) {
        return null;
      }
    
      // Function to calculate Euclidean distance between two points
      function distance(p1, p2) {
        return Math.sqrt((p1[0] - p2[0]) ** 2 + (p1[1] - p2[1]) ** 2);
      }
    
      // Sort points by x-coordinate
      points.sort((a, b) => a[0] - b[0]);
    
      function findClosestPair(pointsSortedByX) {
        const n = pointsSortedByX.length;
    
        // Base case: if the number of points is <= 3, use brute-force method
        if (n <= 3) {
          let minDist = Infinity;
          let closestPair = null;
          for (let i = 0; i < n; i++) {
            for (let j = i + 1; j < n; j++) {
              let dist = distance(pointsSortedByX[i], pointsSortedByX[j]);
              if (dist < minDist) {
                minDist = dist;
                closestPair = [pointsSortedByX[i], pointsSortedByX[j]];
              }
            }
          }
          return closestPair;
        }
    
        // Split points into two halves
        const mid = Math.floor(n / 2);
        const leftHalf = pointsSortedByX.slice(0, mid);
        const rightHalf = pointsSortedByX.slice(mid);
    
        // Recursively find the closest pair in each half
        const leftClosestPair = findClosestPair(leftHalf);
        const rightClosestPair = findClosestPair(rightHalf);
    
        // Find the smaller distance between the closest pairs found in both halves
        const leftMinDist = distance(leftClosestPair[0], leftClosestPair[1]);
        const rightMinDist = distance(rightClosestPair[0], rightClosestPair[1]);
        let minDist = Math.min(leftMinDist, rightMinDist);
        let closestPair = leftMinDist <= rightMinDist ? leftClosestPair : rightClosestPair;
    
        // Consider the points in the strip area around the midpoint
        const midX = pointsSortedByX[mid][0];
        const strip = pointsSortedByX.filter(point => Math.abs(point[0] - midX) < minDist);
    
        // Sort the strip by y-coordinate
        strip.sort((a, b) => a[1] - b[1]);
    
        // Check the strip area for potential closer pairs
        for (let i = 0; i < strip.length; i++) {
          for (let j = i + 1; j < strip.length && (strip[j][1] - strip[i][1]) < minDist; j++) {
            let dist = distance(strip[i], strip[j]);
            if (dist < minDist) {
              minDist = dist;
              closestPair = [strip[i], strip[j]];
            }
          }
        }
    
        return closestPair;
      }
    
      return findClosestPair(points);
    }
    
    // Example usage
    let points = [
      [2, 2], // A
      [2, 8], // B
      [5, 5], // C
      [6, 3], // D
      [6, 7], // E
      [7, 4], // F
      [7, 9]  // G
    ];
    
    console.log(closestPair(points)); // Output: [[6, 3], [7, 4]] or [[7, 4], [6, 3]]
