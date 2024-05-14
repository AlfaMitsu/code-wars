Password Hashes

    package kata
    
    import (
    	"crypto/md5"
    	"encoding/hex"
    )
    
    func PassHash(str string) string {
    	hasher := md5.New()
    	hasher.Write([]byte(str))
    	hash := hasher.Sum(nil)
    	return hex.EncodeToString(hash)
    }
