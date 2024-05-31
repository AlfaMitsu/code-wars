Regex count lowercase letters

    function lowercaseCount(str){
      return (str.match(/[a-z]/g) || []).length;
    }
