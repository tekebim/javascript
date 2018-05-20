# Differentes declarations fonctions

## IIFE

    (function (name) {
      name.init = function () {
        return 'init'
      }
    })(namespace)
    
## Fonction expression

    namespace.mafonction = {
      method1: function () {
        return 'method 1'
      },
      method2: function () {
        return 'method 2'
      }
    }
    
## Arrow fonction
    
    var absValue = (number) => {  
      if (number < 0) {
        return -number;
      }
      return number;
    }
