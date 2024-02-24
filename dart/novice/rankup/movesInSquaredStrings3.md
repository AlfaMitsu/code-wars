Moves in Squared strings 3

    String diag1Sym(String str) {
      List<String> lines = str.split('\n');
      List<String> result = List.generate(lines.length, (index) {
        return List.generate(lines.length, (innerIndex) {
          return lines[innerIndex][index];
        }).join('');
      });
      return result.join('\n');
    }
    
    String rot90Clock(String str) {
      List<String> lines = str.split('\n');
      List<String> result = List.generate(lines.length, (index) {
        return List.generate(lines.length, (innerIndex) {
          return lines[lines.length - innerIndex - 1][index];
        }).join('');
      });
      return result.join('\n');
    }
    
    String selfieAndDiag1(String str) {
      List<String> lines = str.split('\n');
      List<String> diag1SymLines = List.generate(lines.length, (index) {
        return List.generate(lines.length, (innerIndex) {
          return lines[innerIndex][index];
        }).join('');
      });
      List<String> result = List.generate(lines.length, (index) {
        return '${lines[index]}|${diag1SymLines[index]}';
      });
      return result.join('\n');
    }
    
    String oper(String Function(String) fct, String s) {
      return fct(s);
    }
