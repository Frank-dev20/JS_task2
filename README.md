
let data = [
  {principal: 2500, time: 1.8},
  {principal: 1000, time: 5},
  {principal: 3000, time: 1},
  {principal: 2000, time: 3}
  ];
​
​
function interestCalculator(array){
  let interestData = []; //declare empty List
  
  for(let j in array)

 {
    
    interestData.principal = array[j].principal;
    interestData.time = array[j].time;
    interestData.rate;
    interestData.interest;
 
  
  
  if (array[j].principal >= 2500 && array[j].time > 1 && array[j].time < 3) {
     interestData.rate = 3;
     
     
     
    interestData.interest = (interestData.principal * interestData.rate * interestData.time)/100;
  }
  else if (array[j].principal >= 2500 && array[j].time >= 3) {
    interestData.rate = 4;
    
    interestData.interest = (interestData.principal * interestData.rate * interestData.time)/100;
  }
  else if (array[j].principal < 2500 || array[j].time <= 1) {
    interestData.rate = 2;
    
    interestData.interest = (interestData.principal * interestData.rate * interestData.time)/100;
  }
  else {
    interestData.rate = 1;
    
    interestData.interest = (interestData.principal * interestData.rate * interestData.time)/100;
  }
  
  
    interestData.push({principal:interestData.principal, time:interestData.time, rate:interestData.rate, interest:interestData.interest});
  }
  
    console.log(interestData);
    return interestData;
}
​
interestCalculator(data);
