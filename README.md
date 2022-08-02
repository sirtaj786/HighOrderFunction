
---State:-
A state in React Component is its own local state, the state cannot be accessed and modified outside the component and can only be used inside the component which is very similar to, you already guessed it a function own local scope. We can define variables inside the function which can only be used inside the function block scope

--Props:-
Without props, React Component will stop making sense. A React component is a reusable component which can be used over and over again in the UI, but not always we are going to render the same component with same data. Sometimes we have to change the data or content inside a component. That’s why props are introduced in React





**----------------------------******
State API:-useState is a React , which allows us to have state variables in the JSX functional component. we pass an initial value to this function, and it returns a variable with a new state based on functional logic.
 the useState hook allows us to have state variables in the JSX functional component. It takes one argument which is the initial state and returns a state value and a function to update it.
 - Declaration of useState hook
  const [count, setCount] = useState(0)
  *********-----------------------------*****


# HighOrderFunction

Map:-The map() method in JavaScript creates an array by calling a specific function on each element present in the parent array. It is a non-mutating method. Generally map() method is used to iterate over an array and calling function on every element of array.


// created own map method
Array.prototype.myMap=function(callback){
  
    var arr = [];                         
    
    for(let i=0; i<this.length; i++)    
    {
     arr.push(callback(this[i]));       
    }
    
    return arr;                         
   };
   var a=[1,2,3,4,5];
   var r=a.myMap(item=>item*2)
   console.log(r)
   
   
   Filter:-The JavaScript filter array function is used to filter an array based on specified criteria. After filtering it returns an array with the values that pass the filter.

The JavaScript filter function iterates over the existing values in an array and returns the values that pass. The search criteria in the JavaScript filter function are passed using a callbac kfunctionn.

   //Own filter method
   

   Array.prototype.myFilter = function(callback){
 
    var arr = [];                         
    
    for(let i=0; i<this.length; i++)
    {
     if(callback(this[i]) == true)        
     {
      arr.push(this[i]);                  
     }
     
    }
    
    return arr;                           
   }
   var a=[10,23,34,4,50];
   var r=a.myFilter(i=>i>20)
   console.log(r)



Reduce:-Iterating over an array to collect its elements into a single result is a very common use case.

A good example of this is using a for loop to iterate through an array of numbers and add all the numbers togethe


///own reducer

Array.prototype.myReduce = function(callback){
    var a =0;                              
    for(let i=0; i<this.length; i++)       
    {
        callback(a = a+this[i])            
    }
     
    return a;                              
}
var b=[2,4,5,67,8]
var res=b.myReduce((acc,item)=>acc+item)
console.log(res)

 ***map***
 The map() method creates a new array populated with the results of calling a provided function on every element in the calling array.
 const array = [1, 4, 9, 16];


const res = array.map(x => x * 2);

console.log(res);

*****filter***
 filtered down to just the elements from the given array that pass the test implemented by the provided function.
 
 const array = [32, 33, 16, 40];
const result = array.filter(num);

function num(el) {
  return el >= 18;
}

****reduce***
The reduce() method returns a single value: the function's accumulated result.
The reduce() method does not change the original array.

const array = [1, 2, 3, 4];



const sum = array.reduce(
  (previousValue, currentValue) => previousValue + currentValue,
  0
);

console.log(sum);
