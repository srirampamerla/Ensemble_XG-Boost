# Ensemble_XG-Boost
XGBoost (Extreme Gradient Boosting): An optimized implementation of gradient boosting, known for its efficiency and performance.

![Alt text](https://github.com/srirampamerla/Ensemble_XG-Boost/blob/main/xg1.png?raw=true)

Coinsder above dataset
1. Coinsder Base Model(i.e Probability is (0+1/2)=0.5=predicted
2. Calculate Residual(actual-predicted)
3. Construct Decision Tree for all the features which has Gain higher that will be root node.

  ![Alt text](https://github.com/srirampamerla/Ensemble_XG-Boost/blob/main/xg3.png?raw=true)

4. Calcuate similarity  Weight

![Alt text](https://github.com/srirampamerla/Ensemble_XG-Boost/blob/main/xg2.png?raw=true)

5. Calculate Gain. Which tree has Highest Gain take that.
   Gain= Similarity weight of (left tree+right tree- overall or parent similarity weight)
   Here above we calculated and constructed  for both salary and credit Gain. In which salary as higher. So we are coinsdering root node as Salary
 
7. Continue with next feature. Calculate in both left and right leaf. Here for credit we got same gain we are coinsdering anyone

![Alt text](https://github.com/srirampamerla/Ensemble_XG-Boost/blob/main/xg4.png?raw=true)

8. After reaching leaf node we need to calculate new predicted value
   log(odds)=log(p/1-p) for base model

   ![Alt text](https://github.com/srirampamerla/Ensemble_XG-Boost/blob/main/xg6.png?raw=true)

   new predicted value=σ(base model+(learning rate(α) * similarity weight )-> of 1st row salry<=50k and credit=B we need to navigate in this path and coinder that similarity weight.

   ![Alt text](https://github.com/srirampamerla/Ensemble_XG-Boost/blob/main/xg5.png?raw=true)

   Like that calculate for evry row.
10. Again calculate Residual 2(actual-new predicted value) and start from step-1

![Alt text](https://github.com/srirampamerla/Ensemble_XG-Boost/blob/main/xg7.png?raw=true)
   Final =σ(base model+α(DT1)+α(DT2)+......+α(DTn)

   Post pruning--> Core value-> pr(1-pr). if gain< core value then we will get the branch
