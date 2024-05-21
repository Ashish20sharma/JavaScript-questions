# JavaScript-questions

1. Write a function that checks if a given string is a palindrome.
Ans:

        function palindrom(str) {
        let str1='';
        for(let i=str.length-1;i>=0;i--){
          str1+=str[i];
        }
          if(str1===str){
            return true;
          }else{
            return false;
          }
        }
        console.log(palindrom("mam"));
   
2.Implement a function to reverse a string.
Ans:

        function reverseStr(str) {
          let str1='';
        for(let i=str.length-1;i>=0;i--){
          str1+=str[i];
        }
          return str1;
      }
          console.log(reverseStr("ashish"));

3.Write a function that finds the maximum number in an array of numbers.
Ans:

    function maxmin(arr) {
      let max=arr[0];
      let min=arr[0];
    for(let i=0;i<arr.length;i++){
    if(max<arr[i]){
      max=arr[i];
    }else if(min>arr[i]){
      min=arr[i];
    }
    }
      return {max:max,min:min}
    }
      console.log(maxmin([1,5,4,2,4,7,8]));

4.Remove duplicates from an array.
Ans:

    function duplicate(arr) {
        let filteredArr=[];
     for(let i=0;i<arr.length;i++){
        if(!filteredArr.includes(arr[i])){
            filteredArr.push(arr[i])
      }
    }
        return filteredArr;
    }
    console.log(duplicate([1,1,2,4,3,3,5,6]));

5.Write a function that checks if a given number is prime.
Ans:

     function prime(num) {
      if(num<=1){
        return false;
      }
      for(let i=2;i<num;i++){
        if(num%i===0){
          return false;
        }
      }
          return true;
  
      }
        console.log(prime(12));

6.Implement a function to sort an array of numbers in ascending order.
Ans:

    function accending(arr) {
      for(let i=0;i<arr.length;i++){
        for(let j=0;j<arr.length;j++){
          if(arr[j]>arr[j+1]){
            let temp=arr[j];
            arr[j]=arr[j+1];
            arr[j+1]=temp;
          }
        }
      }
      return arr;
    }
    console.log(accending([1,5,4,2,3,6]));

7.Implement a function to find the Fibonacci series up to a given number of terms.
Ans:

    function Fibonacci(fibo) {
      for(let i=0;i<8;i++){
        fibo.push(fibo[i]+fibo[i+1]);
      }
        return fibo;
    }
    console.log(Fibonacci([0,1]))

