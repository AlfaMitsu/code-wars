Human readable duration format

    function formatDuration (seconds) {
      if (seconds === 0) return "now";
      
      const units = {
        year: 365 * 24 * 60 * 60,
        day: 24 * 60 * 60,
        hour: 60 * 60,
        minute: 60,
        second: 1
      };
      
      const parts = [];
      
      for (let unit in units) {
        const value = Math.floor(seconds / units[unit]);
        if (value) {
          parts.push(`${value} ${unit}${value > 1 ? 's' : ''}`);
          seconds -= value * units[unit];
        }
      }
      
      return parts.length > 1 ? parts.join(", ").replace(/,([^,]*)$/, " and$1") : parts[0];
    }
