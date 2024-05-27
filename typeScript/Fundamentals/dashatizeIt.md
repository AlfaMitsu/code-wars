Dashatize it

    export function dashatize(num: number) : string {
      return num.toString()
                .replace(/([13579])/g, "-$1-")   // Add dashes before and after each odd digit
                .replace(/--/g, "-")             // Remove any double dashes
                .replace(/(^-|-$)/g, "");        // Remove leading and trailing dashes
    };
