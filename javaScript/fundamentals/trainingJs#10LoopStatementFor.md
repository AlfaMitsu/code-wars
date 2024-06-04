Training JS #10: loop statement --for

    function pickIt(arr){
      var odd=[],even=[];
      //coding here
      for (var i = 0; i < arr.length; i++) {
        if (arr[i] % 2 === 0) {
          even.push(arr[i]);
        } else {
          odd.push(arr[i]);
        }
      }
      
      return [odd,even];
    }
