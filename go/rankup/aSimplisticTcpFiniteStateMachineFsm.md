A Simplistic TCP Finite State Machine (FSM)

    package kata
    
    func TraverseTCPStates(events []string) string {
    	state := "CLOSED"
    
    	for _, event := range events {
    		switch state {
    		case "CLOSED":
    			switch event {
    			case "APP_PASSIVE_OPEN":
    				state = "LISTEN"
    			case "APP_ACTIVE_OPEN":
    				state = "SYN_SENT"
    			default:
    				return "ERROR"
    			}
    		case "LISTEN":
    			switch event {
    			case "RCV_SYN":
    				state = "SYN_RCVD"
    			case "APP_SEND":
    				state = "SYN_SENT"
    			case "APP_CLOSE":
    				state = "CLOSED"
    			default:
    				return "ERROR"
    			}
    		case "SYN_RCVD":
    			switch event {
    			case "APP_CLOSE":
    				state = "FIN_WAIT_1"
    			case "RCV_ACK":
    				state = "ESTABLISHED"
    			default:
    				return "ERROR"
    			}
    		case "SYN_SENT":
    			switch event {
    			case "RCV_SYN":
    				state = "SYN_RCVD"
    			case "RCV_SYN_ACK":
    				state = "ESTABLISHED"
    			case "APP_CLOSE":
    				state = "CLOSED"
    			default:
    				return "ERROR"
    			}
    		case "ESTABLISHED":
    			switch event {
    			case "APP_CLOSE":
    				state = "FIN_WAIT_1"
    			case "RCV_FIN":
    				state = "CLOSE_WAIT"
    			default:
    				return "ERROR"
    			}
    		case "FIN_WAIT_1":
    			switch event {
    			case "RCV_FIN":
    				state = "CLOSING"
    			case "RCV_FIN_ACK":
    				state = "TIME_WAIT"
    			case "RCV_ACK":
    				state = "FIN_WAIT_2"
    			default:
    				return "ERROR"
    			}
    		case "FIN_WAIT_2":
    			switch event {
    			case "RCV_FIN":
    				state = "TIME_WAIT"
    			default:
    				return "ERROR"
    			}
    		case "CLOSING":
    			switch event {
    			case "RCV_ACK":
    				state = "TIME_WAIT"
    			default:
    				return "ERROR"
    			}
    		case "TIME_WAIT":
    			switch event {
    			case "APP_TIMEOUT":
    				state = "CLOSED"
    			default:
    				return "ERROR"
    			}
    		case "CLOSE_WAIT":
    			switch event {
    			case "APP_CLOSE":
    				state = "LAST_ACK"
    			default:
    				return "ERROR"
    			}
    		case "LAST_ACK":
    			switch event {
    			case "RCV_ACK":
    				state = "CLOSED"
    			default:
    				return "ERROR"
    			}
    		default:
    			return "ERROR"
    		}
    	}
    
    	return state
    }
