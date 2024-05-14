Product of consecutive Fib numbers

    package kata
    
    func ProductFib(prod uint64) [3]uint64 {
    	var a, b uint64 = 0, 1
    	for a*b < prod {
    		a, b = b, a+b
    	}
    	if a*b == prod {
    		return [3]uint64{a, b, 1}
    	}
    	return [3]uint64{a, b, 0}
    }
