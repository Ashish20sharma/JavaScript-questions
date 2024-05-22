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

8. Write a function that checks if two strings are anagrams of each other.
Ans:

        function anagram(str1,str2) {
          if(str1.length!==str2.length){
            return "Not anagram";
          }
  
          const wordCount={};
          for(let item of str1){
            wordCount[item]=(wordCount[item]||0)+1;
          }
  
          for(let item of str2){
            for(let count in wordCount){
              if(item===count){
                wordCount[count]--;
              }
            }
          }
  
          for(let count in wordCount){
            if(wordCount[count]>=1){
              return "Not a anagram";
            }
          }
          return "anagram";
        }
        console.log(anagram("listen","silent"));

9. Write a function to remove all occurrences of a specific element from an array.
Ans:

        function removeElement(arr,element) {
          let newArr=[];
          for(let i=0;i<arr.length;i++){
            if(arr[i]!==element){
              newArr.push(arr[i]);
            }
          }
          return newArr;
        }
        console.log(removeElement([1,2,3,2,4,5,6,2],2));

Second solution:-

        function removeElement(arr,element) {
          let newArr=arr.filter((item)=>{
            return item!==element;
          })
          return newArr;
        }
        console.log(removeElement([1,2,3,2,4,5,6,2],2));
        
10.Write a function that finds the longest word in a sentence.
Ans:

        function findLongestWord(str) {
          let arr=str.split(" ");
          let longest=arr[0];
          for(let i=0;i<arr.length;i++){
            if(longest.length<arr[i].length){
              longest=arr[i];
            }
          }
          return longest;
        }
        console.log(findLongestWord("i am ashish"));

11.Implement a function that merges two sorted arrays into one sorted array.
Ans:

        function mergeSortedArrays(arr1,arr2) {
          let sortedArr=[...arr1,...arr2];
          for(let i=0;i<sortedArr.length;i++){
            for(let j=0;j<sortedArr.length;j++){
              if(sortedArr[j]>sortedArr[j+1]){
                let temp=sortedArr[j];
                sortedArr[j]=sortedArr[j+1];
                sortedArr[j]=temp;
              }
            }
          }
          return sortedArr;
        }
        console.log(mergeSortedArrays([1, 3, 5], [2, 4, 6]));

12.Implement a function to calculate the sum of digits in a number.
Ans:

        function sumOfDigits(num) {
          let arr=String(num).split('');
          let sum=0;
          for(let i=0;i<arr.length;i++){
            sum+=Number(arr[i]);
          }
          return sum;
        }
        console.log(sumOfDigits(12345));

13.Implement a function that finds the second smallest element in an array.
Ans:

        function findSecondSmallest(arr) {
          let max=arr[0];
          let secondMax=null;
          for(let i=0;i<arr.length;i++){
            if(max<arr[i]){
              secondMax=max;
              max=arr[i];
            }
          }
          return {max:max,secondMax:secondMax};
        }
        console.log(findSecondSmallest([1,5,4,2,5,6]));

14.Write a function to reverse the order of words in a sentence.
Ans:

        function reverseWords(str) {
          let arr=str.split(" ");
          let reverse="";
          for(let i=arr.length-1;i>=0;i--){
            reverse+=arr[i]+" ";
          }
          return reverse;
        }
        console.log(reverseWords("Ashish sharma"));

15.Write a function that finds the most frequent element in an array.
Ans:

        function findMostFrequent(arr) {
          let wordCount={};
          for(let item of arr){
            wordCount[item]=(wordCount[item]||0)+1;
          }
  
          let mostFrequentCount=0;
          let mostFrequent;
          for(let item in wordCount){
            if(wordCount[item]>mostFrequentCount){
              mostFrequentCount=wordCount[item];
              mostFrequent=item;
            }
          }
          return mostFrequent;
        }
        console.log(findMostFrequent([1,4,5,7,8,8,8,8,8,8,4,4,4,4]));
