Count IP Addressess

    package kata
    
    import (
        "net"
        "math/big"
    )
    
    func IpsBetween(start, end string) int {
        startIP := big.NewInt(0)
        startIP.SetBytes(net.ParseIP(start).To4())
    
        endIP := big.NewInt(0)
        endIP.SetBytes(net.ParseIP(end).To4())
    
        diff := new(big.Int).Sub(endIP, startIP)
        return int(diff.Int64())
    }
