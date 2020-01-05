# KatasDelivery

## Numbers to Letters

```javascript
    function switcher(str){ 
    var numLetter2 = ["z", "y", "x", "w", "v", "u", "t", "s", "r", "q", "p", "o", "n", "m", "l", "k", "j", "i", "h", "g", "f", "e", "d", "c", "b", "a", "!", "?", " "]; 
    var result = '';
    for (let i = 0; i < str.length; i++){ 
	    let positionArray = parseInt(str[i]);
	    result += numLetter2[positionArray - 1];
    }
    console.log(result);
    return result;
    }
```



## Remove First and Last Character

```javascript    
    function removeChar(str){
	    let withOutFirst = str.substr(1);
	    let result = withOutFirst.slice(0, -1);
	    console.log(result);
		return result;
	};
```

##  Vowel Count

```javascript    
    function getCount(str) { 
	    let vowelsCount = 0;
	    let vowels = ["a","e","i","o","u"];
	    for(var i = 0;i < str.length;i++){
		    for(var j=0;j<vowels.length;j++){
			    if(str[i] === vowels[j]){
			    vowelsCount++;
			    }
			 }
		}
		return vowelsCount;
	}
```

## Sum Mixed Array

```javascript
    function sumMix(x){
	    let result = 0;
	    let num;
	    for (let i = 0; i < x.length; i++){
		    let num = x[i];
		    let numRight= parseInt(num);
		    result += numRight;
		}
		return result;
	}
```

## Count of positives / sum of negatives

```javascript
    function countPositivesSumNegatives(input) {
	    let countPositives = 0;
	    let sumNegatives = 0;
	    let num = 0;
	    let result =[];
	    if(!input) { 
		    return result;
		} 
		for ( let i = 0; i < input.length; i ++) {
			num = input[i];
			if(Math.sign(num) == 1){
				countPositives++; 
			} else {
				sumNegatives += num;
			}
			result = [countPositives, sumNegatives]; 
		}
		return result;
}
```

## Get the mean of an array

```javascript  
    function getAverage(marks){
	    let totalMarks = 0;
	    let result = 0;
	    for ( let i = 0; i < marks.length; i ++) {
		    totalMarks += marks[i];
		}
		result = Math.floor((totalMarks / marks.length));
		return result;
	}
```

## Find numbers which are divisible by given number

```javascript
    function divisibleBy(numbers, divisor){
	    let result = [];
	    for (let i = 0; i < numbers.length; i++) {
		    if (numbers[i] % divisor == 0) {
			    result.push(numbers[i]); 
			}
		}
		return result;
	}
```

## List Filtering

```javascript
    function filter_list(l) {
	    let num = 0;
	    let result = [];
	    for (let i = 0; i < l.length; i++) {
		    num = l[i];
		    if( typeof num == 'number'){
			    result.push(num);
			}
		}
		return result;
	}
```

### Credit Card Mask

```javascript
    function maskify(cc) {
	    let resultBefore = cc.split('');
	    for( let i = 0; i < (cc.length -4); i++) {
		    resultBefore.splice(i,1, '#');
		}
		let result =resultBefore.toString();
		let finalResult; finalResult= result.replace(/,/g, '');
		console.log(finalResult);
		return finalResult;
	}
```

## Flatten

```javascript
    var flatten = function (array){
	    let result = [];
	    for(let i = 0; i < array.length; i++){
		    if(Array.isArray(array[i])){
			    result.push(...array[i]);
			} else {
				result.push(array[i]);
			}
		}
		return result;
	}
```

## Square Every digit

```javascript
    function squareDigits(num){
	    let numArray = String(num).split('');
	    let result = [];
	    for(let  val  of numArray){
		    result.push(Math.pow(parseInt(val), 2));
		}
		result = result.join('');
		return parseInt(result);
	}
```