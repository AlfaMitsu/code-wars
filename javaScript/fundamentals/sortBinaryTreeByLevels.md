Sort Binary Tree by levels

    function treeByLevels(rootNode) {
      if (!rootNode) return [];
    
      const result = [];
      const queue = [rootNode];
    
      while (queue.length > 0) {
        const node = queue.shift();
        result.push(node.value);
    
        if (node.left) queue.push(node.left);
        if (node.right) queue.push(node.right);
      }
    
      return result;
    }
    
    // Example usage
    const tree1 = new Node(2, new Node(8, new Node(1), new Node(3)), new Node(9, new Node(4), new Node(5)));
    console.log(treeByLevels(tree1)); // Output: [2, 8, 9, 1, 3, 4, 5]
    
    const tree2 = new Node(1, new Node(8, null, new Node(3)), new Node(4, new Node(5, new Node(7))));
    console.log(treeByLevels(tree2)); // Output: [1, 8, 4, 3, 5, 7]
