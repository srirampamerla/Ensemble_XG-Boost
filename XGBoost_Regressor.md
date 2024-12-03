# XG Boost Regressor

![Alt text](https://github.com/srirampamerla/Ensemble_XG-Boost/blob/main/xgr.png?raw=true)

Avg of the salary column

![Alt text](https://github.com/srirampamerla/Ensemble_XG-Boost/blob/main/xgr2.png?raw=true)

Check all the splits like 
1. <=2 and >2
2. <=2.5 and >2.5

   Check all the splits calculate similarity weight and gain which has highest gain we can coinsder that as the root node


![Alt text](https://github.com/srirampamerla/Ensemble_XG-Boost/blob/main/xgr3.png?raw=true)

Go to the next feature check which has highest gain that side of the tree we can coinsder

If leaf node reaches take the avg of the actual values


![Alt text](https://github.com/srirampamerla/Ensemble_XG-Boost/blob/main/xgr4.png?raw=true)

Base model will be 51k(avergae)
Go to each and every row calculate predicted value
if two values are belongs same category we can coinsdered predicted value is same

![Alt text](https://github.com/srirampamerla/Ensemble_XG-Boost/blob/main/xgr5.png?raw=true)

Once calculated predicted value
then actual value-predicted value= Residual2

Continue same process 
