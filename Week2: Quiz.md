##Question 1
What is the variance of the distribution of the average an IID draw of n observations from a population with mean μ and variance σ2.

σ2/n

##Question 2
Suppose that diastolic blood pressures (DBPs) for men aged 35-44 are normally distributed with a mean of 80 (mm Hg) and a standard deviation of 10. About what is the probability that a random 35-44 year old has a DBP less than 70?

value2<- 70;
mean2<- 80;
sd2<- 10;
answ2<-pnorm(value2, mean2, sd2);
round(answ2, 2)


##Question 3
Brain volume for adult women is normally distributed with a mean of about 1,100 cc for women with a standard deviation of 75 cc. About what brain volume represents the 95th percentile?

quantil3<- 0.95;
mean3<- 1100;
sd3<- 75;
answ3<-qnorm(quantil3, mean3, sd3);
round(answ3,0)


##Question 4
Refer to the previous question. Brain volume for adult women is about 1,100 cc for women with a standard deviation of 75 cc. Consider the sample mean of 100 random adult women from this population. Around what is the 95th percentile of the distribution of that sample mean?

mean4<- 1100;
sd4<- 75;
n4<- 100;
var4<- sd4/sqrt(n4);
quantile4<- 1.645;
answ4<- mean4+(var4*quantile4);
answ4


##Question 5
You flip a fair coin 5 times, about what's the probability of getting 4 or 5 heads?

prob4<- choose(5,4)*0.5^4*(1-0.5)^1;
prob5<- choose(5,5)*0.5^5*(1-0.5)^0;
answ5<- prob4+prob5;
round(answ5,2)


##Question 6
The respiratory disturbance index (RDI), a measure of sleep disturbance, for a specific population has a mean of 15 (sleep events per hour) and a standard deviation of 10. They are not normally distributed. Give your best estimate of the probability that a sample mean RDI of 100 people is between 14 and 16 events per hour?

mean6<- 15;
sd6<- 10;
value6a<- (14-mean6)/(sd6/sqrt(100));
p14<-pnorm(value6a);
value6b<- (16-mean6)/(sd6/sqrt(100));
p16<-pnorm(value6b);
answ6<-p16-p14;
round(answ6,2)


##Question 7
Consider a standard uniform density. The mean for this density is .5 and the variance is 1 / 12. You sample 1,000 observations from this distribution and take the sample mean, what value would you expect it to be near? Give your answer to at least one decimal place.

mean(rnorm(1e+07, mean = 0.5, sd = sqrt(1/12)))


##Question 8
The number of people showing up at a bus stop is assumed to be Poisson with a mean of 5 people per hour. You watch the bus stop for 3 hours. What's the probability of viewing 10 or fewer people? Express your answer to at least two decimal places

round(ppois(10, lambda = 5 * 3), 2)
