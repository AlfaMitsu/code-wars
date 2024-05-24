Int 32 to IPv4

    function int32ToIp(int32){
      return [
        (int32 >> 24) & 255,
        (int32 >> 16) & 255,
        (int32 >> 8) & 255,
        int32 & 255
      ].join('.');
    }
    
    // Examples
    console.log(int32ToIp(2149583361)); // Output: "128.32.10.1"
    console.log(int32ToIp(32)); // Output: "0.0.0.32"
    console.log(int32ToIp(0)); // Output: "0.0.0.0"
