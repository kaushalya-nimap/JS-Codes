# JS-Codes
================================================================================================================================================================================
Code 1: Remove Duplicate characters from String
function removeDuplicateCharacters() {
  var string='priya riya supriya'
  let result= string.split('').filter((item, index, arr)=> {
               return arr.indexOf(item) == index;
               }).join('');
  return result;
}
console.log(removeDuplicateCharacters());
================================================================================================================================================================================
Code 2: Remove Duplicate characters from array of element and find the count of an elements using set object
var arr = [55, 44, 55,67,67,67,67,8,8,8,8,8,65,1,2,3,3,34,5];
var unique = [...new Set(arr)]
console.log(unique) //output: [55, 44, 67, 8, 65, 1, 2, 3, 34, 5]
console.log(unique.length) //output: 10
================================================================================================================================================================================
Code 3: Remove Duplicate characters from array of element using filter
var myArray = ['a', 1, 'a', 2, '1'];
var unique = myArray.filter((value, index, arr) => arr.indexOf(value) === index);
================================================================================================================================================================================
Code 4:String reverse without reversing of individual words (Array of elements can be reverse with reverse() method but for string it is not possible so required to split 
and then join().
METHOD 1:-
function removeDuplicates(){
   var string ="India is my country"
   let result = string.split('').reverse().join('').split(' ').reverse().join(' ')
   return result
}
console.log(removeDuplicates()) 
output = "aidnI si ym yrtnuoc"

METHOD 2:-
function removeDuplicates() {
    var string = "India is my country";
    let reversedString = ""; 
    for (let i = string.length - 1; i >= 0; i--) {
        reversedString += string[i];
    }
    let result = ""; 
    let word = "";  
       for (let i = 0; i < reversedString.length; i++) {
        if (reversedString[i] !== " ") {
            word += reversedString[i]; // Build the word character by character
        } else {
            result = word + " " + result; // Add the reversed word at the start of the result
            word = ""; // Reset the word
        }
    }
result = word + " " + result;
return result.trim();
}
console.log(removeDuplicates());
output = "aidnI si ym yrtnuoc"
================================================================================================================================================================================
Code 5:String reverse with reversing of individual words
function withoutReverse(){
   var string ="India is my country"
   let result = string.split('').reverse().join('')
   return result
}
console.log(withoutReverse())
output = "yrtnuoc ym si aidnI"
================================================================================================================================================================================
Code 6:String reverse without using inbult function
function Reverse(){
   var string ="India is my country";
   var result="";
   for( var i=string.length-1; i>=0 ; i-- ) {
      result=result+string[i] }
   return result
}
console.log(Reverse())
output = "yrtnuoc ym si aidnI"
================================================================================================================================================================================
Code 7: Find factorial of user input number
const number = parseInt(prompt('Enter a positive integer: '));
if (number < 0) { console.log('Error! Factorial for negative number does not exist.')}
else if (number === 0) { console.log(`The factorial is 1.`)}
else {
    let fact = 1;
    for (i = 1; i <= number; i++) {
        fact *= i;
    }
    console.log(`The factorial is ${fact}.`);
}
================================================================================================================================================================================
Code 8:Anagram
function checkStringsAnagram() {
var a="Army";
var b="Mary"
   let str1 =  a.toLowerCase().split('').sort().join('');
   let str2 =  b.toLowerCase().split('').sort().join('');
   if(str1 === str2){
      console.log("True");
   } 
   else { 
      console.log("False");
   }
}
================================================================================================================================================================================
Code 9: Swapping of 2 numbers with third variable
let a=10;
let b=20;
let c;
   c=a;
   a=b;
   b=c;
console.log (a,b,c)
================================================================================================================================================================================
Code 10: Swapping of 2 numbers without third variable
let a=10; 
let b=20;
   a=a+b //30
   b=a-b //10
   a=a-b //20
console.log (a,b)
================================================================================================================================================================================
Code 11: To check the string or number is palindrome or not( ex: 121,madam,anna) using reverse method
function checkPalindrome(){
  const string = "anmna"
  let arr= string.split('').reverse().join('')
  //console.log(arr)
  if (string==arr){
      console.log("Palindrome")
  }
  else{
      console.log("Not Palindrome")
  }
}
checkPalindrome()
================================================================================================================================================================================
Code 12: To find longest word from a string using (for of) /*for(var i=0; i>=num; i++) means iterate by indexing*/  /*for (var word of words) means iterate by an elements not 
by indexing*/
function longestWord(){
   let string = "supriya is a masooooom good girl"
   var words= string.split(' ')
   var longest=" "
   for(var word of words){
        console.log(word)
        if (word.length > longest.length)
        {
            longest=word;
         }
   }
    return longest.length
}
longestWord()
---------------------------
function longestWord(){
   let string = "supriya is a hahahahaha good girl"
   var arr= string.split(' ')
   var longest=" "
   for(var i=0; i<arr.length; i++){
      
        if (arr[i].length > longest.length)
        {
            longest=arr[i];
        }
   }
   return longest
}
console.log(longestWord())
================================================================================================================================================================================
Code 13: To find longest word from a string using functions
function findLongestWord() {
  var str = "Priya is a goog girl and having hardworking skill"
  var longestWord = str.split(' ').sort((a, b) => {return b.length - a.length }); //in desc order //from greater to smallest word
     console.log(longestWord[0]);
     console.log(longestWord[0].length); 
}
findLongestWord();
================================================================================================================================================================================
Code 14: To find longest common string from array of strings
function longestCommonString(){
  array=["go","google","gosh"]
  var arr = array.sort()
  var i=0;
  while(arr[0].length>0 && arr[0].charAt(i)===arr[arr.length-1].charAt(i)){
    i++;
  }
  console.log(arr[0].substring(0,i)) // "go"
  return arr[0].substring(0,i)
}
longestCommonString() 
--------------------------------------------------------------------
function longestCommonString(){
 let array=["go","google","gosh"]
  var arr = array.sort((a,b)=>a.length-b.length)
  let result =""
  for(let i=0; i<arr[0].length; i++){
    if(arr[0][i]===arr[arr.length-1][i]){
      result+=arr[0][i]
    }
  }
  return result
}
console.log(longestCommonString())
================================================================================================================================================================================
Code 15: To find vowels and its count in a given string
function vowelCounts(){
  vowels=["a","i","e","o","u"]
  var str ="priya"
  count=0;
  for(var letter of str.toLowerCase())
  {
    if(vowels.includes(letter))
    {
      count++;
      console.log(letter)
    }
  }
  console.log(count)
  return count
}
vowelCounts()
================================================================================================================================================================================
Code 16:To find character occurance fro the string
function characterOccurance(str,letter){
   let count =0;
  for(var i=0; i<str.length-1; i++){
    if(str.charAt(i)===letter)
      {
        count++
      }
  }
  console.log(count)
  return count
}
characterOccurance("priyapri", "p")
================================================================================================================================================================================
Code 17: To find a first pair whose sum is zero
function getSumPairZero(array)
{
  for(let number of array)
  {
     for(let i=1; i<array.length; i++)
     {
         if(number+array[i]===0)
         {
            return [number, array[i]]
         }
     }
  }
}
const result = getSumPairZero([-5,-4,-3,-2,-1,0,1,2,3,4,5])
console.log(result)
================================================================================================================================================================================
Code 18:To find the largest pair of the 2 elements using indexing with unsorted elements
function largestPairSumofTwo(numbers){
    const num = numbers.sort((a, b) => b - a);
    console.log(num)
    return num[0] + num[1];
}
const result = largestPairSumofTwo([9,7,8,4,5,6,1,2,3])
console.log(result)
================================================================================================================================================================================
Code 19:To find unique values from 2 arrays and keep into one array.
function uniqueElements(arr1,arr2){
   let arr =[...arr1,...arr2];
   let array =[...new Set(arr)]
   console.log(array)
}
uniqueElements([1,2,3,4,4],[2,3,4,5,6])
================================================================================================================================================================================
Code 20:Write a program that prints the numbers from 1 to 100. But for multiples of three, print "Fizz" instead of the number, and for the multiples of five, print "Buzz". 
For numbers which are multiples of both three and five, print "FizzBuzz"
for (var i=1; i <= 20; i++)
{
    if (i % 15 == 0)
        console.log("FizzBuzz");
    else if (i % 3 == 0)
        console.log("Fizz");
    else if (i % 5 == 0)
        console.log("Buzz");
    else
        console.log(i);
}
================================================================================================================================================================================
Code 21:Uppercase of each first letter of a words 
function upperCaseFirsstLetter(){
   var string ="India is my country";
   var words = string.toLowerCase().split(" ")
   for( var i=0; i<words.length; i++) {
      words[i]=words[i][0].toUpperCase() + words[i].slice(1) //slice is used here to give all the letters except first letter.
      }
   return words.join(" ")
}
console.log(upperCaseFirsstLetter())
================================================================================================================================================================================
Code 22: Uppercase of each first letter of a words using map function
function upperCaseFirsstLetter(){
   var string ="India is my country";
   var words = string.toLowerCase().split(" ").map((ele)=>{
               return ele[0].toUpperCase() + ele.slice(1)
   })
   return words.join(" ")
}
console.log(upperCaseFirsstLetter())
================================================================================================================================================================================
Code 23: To check ending of the string with given character/s using inbuild function
function confirmEnding(str,target){
   return str.endsWith(target) //true
}
console.log(confirmEnding("priya","a"))
===============================================================================================================================================================================
Code 24:To find the largest elements fro the 2 dimensional array 
function largestFromArray(arr){
   var max=[];
   for(var i=0; i<arr.length;i++){
     var tempMax =arr[i][0] //first elements of the 4 internal arrays i,e(1,5,45,89
     for(var j=0; j<arr[i].length; j++){
        var currElement = arr[i][j];
        if(currElement>=tempMax){
          tempMax = currElement
        }
     }
      max.push(tempMax)
   }
  console.log(max)
   return max;
}
largestFromArray([[1,2,3,4],[5,6,7,9],[45,76,2,1],[89,90,87,9]])
-----------
METHOD 2
---
function largestFromArray(arr){
   var max=[0,0,0,0];
   for(var i=0; i<arr.length;i++){
      for(var j=0; j<arr[i].length; j++)
      {
          if(arr[i][j]>=max[i]){
          max[i] = arr[i][j]
        }
      }
   }
  console.log(max)
  return max;
}
---Method 3
function largestFromArray(arr){
    return arr.map((subArray)=>Math.max(...subArray))
}
largestFromArray([[1,2,3,4],[5,6,7,9],[45,76,2,1],[89,90,87,9]])
================================================================================================================================================================================
Code 25:To print a string n number of times.
function repeatStrinNumTimes(str, num){
if (num<1) return ""
return str.repeat(num)
}
console.log(repeatStrinNumTimes("priya",3))
----
METHOD 2
function repeatStrinNumTimes(str, num){
var final="";
if(num<0) return ""
for(var i=0; i<num;i++)
{
  final=final+str
}
return final
}
console.log(repeatStrinNumTimes("priya",3))
================================================================================================================================================================================
Code 26:Truncate a string using slice method
function truncateString(str, num){
if(num<=3) return str.slice(0,num)
return str.slice(0,num-3)+"..." //retuen only 4 digits thats why subtracted from 3
}
console.log(truncateString("priyabagde",2)) //pr
console.log(truncateString("priyabagde",4)) //p... //retuen only 4 digits
================================================================================================================================================================================
Code 27: Converting one dimensional array into n dimensional array using slice
function chunkArrayInGroup(arr, size){
  var group=[]
  while(arr.length>0){
  group.push(arr.slice(0, size))
  arr = arr.slice(size)
  }
  return group
}
console.log (chunkArrayInGroup(['a','b','c','d'],2)) //[["a", "b"], ["c", "d"]]
================================================================================================================================================================================
Code 28:To find only truthy values
function removeFalseValue(arr){
 var trueth = []
 for (var item of arr){
   if(item){
      trueth.push(item)
   }
 }
 return trueth
}
console.log(removeFalseValue(["priya", 0 ,"", false, null,undefined, "ate", Nan ,9 ])) //["priya","ate",9]
---
METHOD 2
function removeFalseValue(arr){
  return arr.filter((item)=>{
                return item})
}
console.log(removeFalseValue(["priya", 0 ,"", false, null,undefined, "ate", 9 ]))
================================================================================================================================================================================
Code 29:Checking all letters from second word present in first word.
function characterPresent(arr){
  var first = arr[0].toLowerCase()
  var second = arr[1].toLowerCase()
  for (var letter of second){
    if(!first.includes(letter)){
      return false
    }
  }
  return true
}
console.log(characterPresent(["hello","hey"]))
---METHOD 2
function characterPresent(arr){
  var first = arr[0].toLowerCase()
  var second = arr[1].toLowerCase()
  for (var letter of second){
    if(first.indexOf(letter)== -1){ //-1 means not found in array
      return false
    }
  }
  return true
}
console.log(characterPresent(["hello","he"]))
-------METHOD 3
function characterPresent(arr){
  var first = arr[0].toLowerCase()
  var second = arr[1].toLowerCase()
  for (var i=0; i<second.length; i++){
    if(!first.includes(second[i])){ //-1 means not found in array
      return false
    }
  }
  return true
}
console.log(characterPresent(["hello","he"]))
================================================================================================================================================================================
Code 30:Remove duplicate that is display unique elements from 2 array by merging or concating both the array
function uniquefromArrays(arr1, arr2){
 let arr = [...arr1, ...arr2]
 let unique = [...new Set(arr)];
 return unique
}
console.log(uniquefromArrays([1,2,3,4], [2,3,4,5])) //[1,2,3,4,5]
================================================================================================================================================================================
Code 31: To add all elements of array OR to add the elements between the smallest and the biggest value in an array
function sumFromStartToEnd(arr){
   // let min=Math.min(...arr)
    //let max=Math.max(...arr)
    //let sum=0
    //for(let i=min;i<=max;i++){
        sum=sum+i
    }
    return sum
    OR
    return arr.reduce((acc,cur)=>acc+cur)
}
console.log(sumFromStartToEnd([1,4,9,10]))
================================================================================================================================================================================
Code 32:Remove or Delete elements from an array using various ways
Way 1: Removing Elements from End of a JavaScript Array
       var ar = [1, 2, 3, 4, 5, 6]; 
       ar.length = 4; // set length to remove elements
       console.log( ar ); // [1, 2, 3, 4]   
Way 2: Removing Elements from Beginning of a JavaScript Array
        var ar = ['zero', 'one', 'two', 'three'];
        ar.shift(); // returns "zero"
        console.log( ar ); // ["one", "two", "three"]        
Way 3: Using Splice to Remove Array Elements in JavaScript
        var list = ["bar", "baz", "foo", "qux"];
        list.splice(0, 2); // Starting at index position 0, remove two elements ["bar", "baz"] and retains ["foo", "qux"].        
Way 4: Removing Array Items By Value Using Splice
       var arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 0];
       for( var i = 0; i < arr.length; i++){ 
           if ( arr[i] === 5) { 
              arr.splice(i, 1); 
           }
       } // [1, 2, 3, 4, 6, 7, 8, 9, 0]      
       OR       
        var arr = [1, 2, 3, 4, 5, 5, 6, 7, 8, 5, 9, 0];
        for( var i = 0; i < arr.length; i++){                             
        if ( arr[i] === 5) { 
            arr.splice(i, 1); 
            i--; 
          }
        } // [1, 2, 3, 4, 6, 7, 8, 9, 0]       
Way 5: Using the Array filter Method to Remove Items By Value
        var array = [1, 2, 3, 4, 5, 6, 7, 8, 9, 0];
        var filtered = array.filter(function(value, index, arr){ 
        return value > 5;
        }); //filtered => [6, 7, 8, 9]  
Way 6: Making a Remove Method
       function arrayRemove(arr, value) { 
        return arr.filter(function(ele){ 
            return ele != value; 
        });
    }
    var result = arrayRemove(array, 6); // result = [1, 2, 3, 4, 5, 7, 8, 9, 0]   
Way 7: Explicitly Remove Array Elements Using the Delete Operator
         var ar = [1, 2, 3, 4, 5, 6];
         delete ar[4]; // delete element with index 4
         console.log( ar ); // [1, 2, 3, 4, undefined, 6]
================================================================================================================================================================================







