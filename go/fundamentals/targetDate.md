Target Date

    package kata
    
    import (
    	"time"
    )
    
    // DateNbDays calculates the date when the initial amount a0 reaches or exceeds the amount a given the interest rate p.
    func DateNbDays(a0 int, a int, p int) string {
    	// Convert the percentage rate to a daily interest rate
    	dailyRate := float64(p) / 36000.0
    	amount := float64(a0)
    	target := float64(a)
    	days := 0
    
    	// Calculate the number of days required for the amount to reach or exceed the target
    	for amount < target {
    		amount += amount * dailyRate
    		days++
    	}
    
    	// Starting date is January 1, 2016
    	startDate := time.Date(2016, 1, 1, 0, 0, 0, 0, time.UTC)
    
    	// Calculate the target date by adding the number of days
    	targetDate := startDate.AddDate(0, 0, days)
    
    	// Return the date in the format "YYYY-MM-DD"
    	return targetDate.Format("2006-01-02")
    }
