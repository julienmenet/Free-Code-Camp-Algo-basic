# Free-Code-Camp-Algo-basic
My solutions for the free code camp basic Algorithms

Reverse a String
---------------------------
    function reverseString(str) {
    return str.split('').reverse().join('');
    }
 
    reverseString("hello");
   
Factorialize a Number
---------------------------
    function factorialize(num) {
    if (num < 0) {
    return -1;
    }
    if (num === 0) {
    return num + 1;
    }
    if (num > 0) {
    return num * factorialize(num - 1);
    }
    }
    factorialize(5);

Check for Palindromes
---------------------------

    function palindrome(str) {
  
    var rev = str;
  
    return rev.replace(/[\W_]/g, '').split('').reverse().join('').toLowerCase() === str.replace(/[\W_]/g, '').toLowerCase();
    }
    palindrome("never odd or even");
    
Find the Longest Word in a String
---------------------------
    function findLongestWord(str) {
    var arrayOfStr = str.split(' ');
    arrayOfStr.sort(function (a, b) {
        return b.length - a.length;
    });
    return arrayOfStr[0].length;
    }
    findLongestWord("The quick brown fox jumped over the lazy dog");

Title Case a Sentence
---------------------------
    function titleCase(str) {
    var arrayMaker = str.toLowerCase().split(' ');
    for (var i = 0; i < arrayMaker.length; i++) {
    arrayMaker[i] = arrayMaker[i].charAt(0).toUpperCase() + arrayMaker[i].substring(1);     
    }
 
         

    return arrayMaker.join(' ');
    }

    titleCase("sHoRt AnD sToUt");

Return Largest Numbers in Arrays
---------------------------
    function largestOfFour(arr) {

    var max=[];
    for(var i=0; arr.length>i; i++ )
    max.unshift(Math.max.apply(Math, arr[i]));
    return max.reverse([]);}

    largestOfFour([[4, 5, 1, 3], [13, 27, 18, 26], [32, 35, 37, 39], [1000, 1001, 857, 1]]);
    
Confirm the Ending
---------------------------
    function confirmEnding(str, target) {
    return str.substring(str.length-target.length) === target;
 
    }

    confirmEnding("Bastian", "n");
    
Repeat a string repeat a string
-------------------------
    function repeatStringNumTimes(str, num) {
     if (num > -1)
     return str.repeat(num);
     else
      return "";
    }

    repeatStringNumTimes("abc", 3);
    
Truncate a string
-------------------------
    function truncateString(str, num) {
    var cut ="";
    if (num < 3)
     return str.slice(0,num)+"...";
     else if (str.length > num)
      return str.slice(0, num-3) + "...";
  
     else 
     return str;
    }

    truncateString("A-", 1);
    
Chunky Monkey
-----------------------

    function chunkArrayInGroups(arr, size) {
     var pop = [];
     for (i=0; i<arr.length;)
      pop.push(arr.slice(i,i+=size));  
  
  
     return pop;
    }

    chunkArrayInGroups(["a", "b", "c", "d"], 2);
    
Slasher Flick
----------------------
    function slasher(arr, howMany) {
    arr.splice(0, howMany);
    return arr;
    }

    slasher([1, 2, 3], 2);
    
Mutations
----------------------
    function mutation(arr) {
     var pop = arr[0].toLowerCase();
     var pop2 = arr[1].toLowerCase();
  
     for (i=0;i<pop2.length;i++) {
     if (pop.indexOf(pop2[i]) < 0) 
     return false;
  
    }
     return true;
  

    }
    mutation(["hello", "HellO"]);
    
Falsy Bouncer
--------------------
    function bouncer(arr) {
     var pop = arr.filter(Boolean);
    return pop;
    }

    bouncer([7, "ate", "", false, 9]);
    
Seek and Destroy
--------------------
    function destroyer(arr) {

    var pop = Array.prototype.slice.call(arguments);
    pop.splice(0, 1) ;
    return arr.filter(function(gone, index) {
    return pop.indexOf(gone) < 0;
    
    });
    
    }

    destroyer([4, 2, 3, 2, 3,1], 2, 3);
    
Where do I belong
--------------------
    function getIndexToIns(arr, num) {
     arr.push(num);
     arr.sort(function(a, b){return a-b;});
  
     return arr.indexOf(num);
      }

    getIndexToIns([40, 60,5], 50);
    
Caesars Cipher
--------------------
    function rot13(str) { // LBH QVQ VG!
     var hold = '';
     for (var i in str) 
      if (str.charCodeAt(i) > 91) {
            hold += str[i];
        }
    else if (str.charCodeAt(i) < 65) {
            hold += str[i];
        }
    else if (str.charCodeAt(i) < 78) {
            hold += String.fromCharCode(str.charCodeAt(i) + 13);
        }
    else {
            hold += String.fromCharCode(str.charCodeAt(i) - 13);
        }
    
    return hold.split('\-').join(' ');
    }

    // Change the inputs below to test
    rot13("SERR CVMMN!");



