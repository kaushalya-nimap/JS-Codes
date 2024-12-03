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
Code 4:String reverse without reversing of individual words (Array of elements can be reverse with reverse() method but for string it is won't possible so required to split 
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

