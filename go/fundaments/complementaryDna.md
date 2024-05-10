Complementary DNA

    package kata
    
    func DNAStrand(dna string) string {
        complement := make(map[byte]byte)
        complement['A'] = 'T'
        complement['T'] = 'A'
        complement['C'] = 'G'
        complement['G'] = 'C'
    
        result := make([]byte, len(dna))
        for i := 0; i < len(dna); i++ {
            result[i] = complement[dna[i]]
        }
    
        return string(result)
    }
