# Differentes declarations fonctions

## IIFE

    (function (name) {
      name.init = function () {
        return 'init'
      }
    })(namespace)
    
## Module pattern

    var namespace = function () {
        // set up private data
        var arr = []; // not visible outside
        for(var i=0; i<4; i++) {
            arr.push(i)
        }
        return {
            // read-only access via getter
            get values() {
                return arr
            }
        }
    }()
    
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
    
## Arrow bis
    
    const SITE = window.SITE || {}

        SITE.navigation = () => {
        };

        SITE.homePage = () => {	
        };

        SITE.portfolioPage = () => {
        };
    
### Exemple

    (function($) {

        var namespace;

        namespace = {
            something : function() {
                alert('hello there!');
            },
            bodyInfo : function() {
                alert($('body').attr('id'));
            }
        };

        window.ns = namespace;

    })(this.jQuery);

    $(function() {
        ns.something();
        ns.bodyInfo();
    });


### Arrow functions examples

    window.name = "global";

    var person = {
        name: "jason",

        shout: function () {
            console.log("my name is ", this.name);
        },
        shout2: () => {
            console.log("my name is ", this.name);
        },
        // Shorter syntax
        shout3() {
            console.log("my name is ", this.name);
        }
    };

    person.shout();  // "jason"
    person.shout2(); // "global"
    person.shout3(); // "jason"
