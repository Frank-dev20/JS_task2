
let data = [
  {principal: 2500, time: 1.8},
  {principal: 1000, time: 5},
  {principal: 3000, time: 1},
  {principal: 2000, time: 3}
//Keys
  ];


 //function

function interestCalculator (array) {
            let rate;
            let interest;
            let interestData = [];

            for(var i = 0; i < array.length; i++) {
                if (array[i].principal >= 2500 && array[i].time > 1 && array[i].time < 3) {
                    rate = 3;

                }else if (array[i].principal >= 2500 && array[i].time >= 3) {
                    rate = 4;
                    
                }else if (array[i].principal < 2500 && array[i].time <= 1) {
                    rate = 2;
                    
                }else {
                    rate = 1;
                } 
         //InterestFormular
          
                interest = (array[i].principal * rate * array[i].time) / 100;
                
                interestData.push({
                        principal: array[i].principal,
                        time: array[i].time,
                        rate: rate,
                        interest: interest
                    });

                console.log(interestData);
            
            }
            return interestData;
        }

        interestCalculator(data);
