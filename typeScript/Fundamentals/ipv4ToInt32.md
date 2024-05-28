IPV4 to Int32

    export function ipToInt32(ip: string): number {
      const octets = ip.split('.').map(Number);
      return (octets[0] << 24) + (octets[1] << 16) + (octets[2] << 8) + octets[3] >>> 0;
    }
    
    // Test
    console.log(ipToInt32("128.32.10.1")); // Output: 2149583361
