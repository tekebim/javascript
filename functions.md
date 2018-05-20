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
    
## Autre format

    (function () {
      var id = 0
      this.next = function () {
        console.log(id++)
      }
    }).apply(namespace.method)
    
## Arrow fonction
    
    var absValue = (number) => {  
      if (number < 0) {
        return -number;
      }
      return number;
    }
