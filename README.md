## Coding Exercise - validateLISPCode()- It validates parenthesis are appropriate and properly nested. It accepts single string parameter and returns boolean. 

function validateLISPCode(str){
  let arr = str.split('').filter(e=>e==='(' || e=== ')' )
  let tArr = []
  if (arr.length%2) return false;
  
  for (let i=0;i<arr.length;i++){
    if (arr[i]==='('){
      tArr.push(arr[i])
    } else {
     if(!tArr.pop()+arr[i]==='()') return false
    }
  }
  
 return tArr.length>0?false: true;
 
}



