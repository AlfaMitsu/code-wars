Recover a secret string from random triplets
    
    var recoverSecret = function(triplets) {
      const graph = new Map();
    
      // Build the graph
      for (let triplet of triplets) {
        for (let i = 0; i < triplet.length; i++) {
          const node = triplet[i];
          if (!graph.has(node)) {
            graph.set(node, new Set());
          }
        }
    
        for (let i = 0; i < triplet.length - 1; i++) {
          const from = triplet[i];
          const to = triplet[i + 1];
          graph.get(from).add(to);
        }
      }
    
      // Perform topological sort
      const result = [];
      const visited = new Set();
    
      const dfs = (node) => {
        if (visited.has(node)) return;
        visited.add(node);
    
        if (graph.has(node)) {
          for (let neighbor of graph.get(node)) {
            dfs(neighbor);
          }
        }
    
        result.unshift(node);
      };
    
      for (let node of graph.keys()) {
        dfs(node);
      }
    
      return result.join('');
    };
    
    // Example usage
    const triplets = [
      ['t', 'u', 'p'],
      ['w', 'h', 'i'],
      ['t', 's', 'u'],
      ['a', 't', 's'],
      ['h', 'a', 'p'],
      ['t', 'i', 's'],
      ['w', 'h', 'a']
    ];
    
    console.log(recoverSecret(triplets)); // Output: 'whatisup'
