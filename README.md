# HighOrderFunction
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

   //filter method
   

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
