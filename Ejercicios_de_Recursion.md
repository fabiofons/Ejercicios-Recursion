# Ejercicios de Recursión
**Factorial**

    function factorial(num){
      if(num === 1){
        return 1;
      } 
      return num * factorial(num - 1); 
    }

**Fibonacci**

    function fibonacci(n){
      if ((n === 1) || (n === 0)) return 1;
      return fibonacci(n-1) + fibonacci(n-2);
    }

**Flatten**

    function flatten(arr) {
      let newArr = [];
      arr.forEach((value) => {
        if(Array.isArray(value)) {
          newArr = newArr.concat(flatten(value));
        }else {
          newArr.push(value);
        } 
      }); 
    return newArr;
    }

**Collatz**

    function collatz(num) {
      if(num / 2 === 1) return 1;
      if(num % 2 == 0){
        num = num / 2;
      }else {
        num = (3 * num) + 1;
      }
      return 1 + collatz(num);
    }

**Pascal**

    function pascaltri(row, col){
      if((row == 0) || (col == row)) return 1;
      return pascaltri(row - 1, col - 1) + pascaltri(row, col - 1);
    }
    
    function pascal(num) {
      let tri = '';
      for(let col = 0; col < num; col++){
        for(let row = 0; row < col + 1; row++) {
          tri += pascaltri(row, col) + " ";
        }
        tri += "\n"; 
      }
      return tri;
    }

