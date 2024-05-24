Can you get the loop?

    function loop_size(node) {
      let tortoise = node.getNext();
      let hare = node.getNext().getNext();
      
      // Find the meeting point
      while (tortoise !== hare) {
        tortoise = tortoise.getNext();
        hare = hare.getNext().getNext();
      }
      
      // Find the start of the loop
      let start = node;
      while (start !== tortoise) {
        start = start.getNext();
        tortoise = tortoise.getNext();
      }
      
      // Find the length of the loop
      let length = 1;
      tortoise = tortoise.getNext();
      while (tortoise !== start) {
        length++;
        tortoise = tortoise.getNext();
      }
      
      return length;
    }
