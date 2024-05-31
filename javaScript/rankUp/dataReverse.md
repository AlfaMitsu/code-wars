Data Reverse

    function dataReverse(data) {
      const segmentLength = 8; // Each segment is 8 bits long
      const segments = [];
    
      // Split the data array into chunks of 8 bits
      for (let i = 0; i < data.length; i += segmentLength) {
        const segment = data.slice(i, i + segmentLength);
        segments.push(segment);
      }
    
      // Reverse the order of the segments
      segments.reverse();
    
      // Flatten the array of segments back into a single array
      const reversedData = segments.flat();
      
      return reversedData;
    }
    
    // Example usage:
    const data = [1,1,1,1,1,1,1,1,0,0,0,0,0,0,0,0,0,0,0,0,1,1,1,1,1,0,1,0,1,0,1,0];
    console.log(dataReverse(data)); // Output: [1,0,1,0,1,0,1,0,0,0,0,0,1,1,1,1,0,0,0,0,0,0,0,0,1,1,1,1,1,1,1,1]
