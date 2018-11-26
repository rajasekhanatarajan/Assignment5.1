# Assignment5.1

#1.If Z is norm (mean = 0, sd = 1)

a) Find P(Z > 2.64)

b) Find P(|Z| > 1.39)

->

a) 0.9958547

b) 0.9177356

#2.Suppose p = the proportion of students who are admitted to the graduate school of the University of California at Berkeley, and suppose that a public relation officer boasts that UCB has historically had a 40% acceptance rate for its graduate school. Consider the data stored in the table UCBAdmissions from Assuming these observations constituted a simple random sample, are they consistent with the officerâ..s claim, or do they provide evidence that the acceptance rate was significantly less than 40%? Use an Î± = 0.01 significance level.

->

qnorm(0.99)

[1] 2.326348

A <- as.data.frame(UCBAdmissions)

head(A)

Admit Gender Dept Freq

1 Admitted Male A 512

2 Rejected Male A 313

3 Admitted Female A 89

4 Rejected Female A 19

5 Admitted Male B 353

6 Rejected Male B 207

xtabs(Freq ~ Admit, data = A)

Admit

Admitted Rejected

1755 2771

phat <- 1755/(1755 + 2771)

(phat - 0.4)/sqrt(0.4 * 0.6/(1755 + 2771))

[1] -1.680919

We fail to reject the null hypothesis as the true proportion of students admitted to graduate school is less than 40% and it shows data are consistent with officer’s claim at I = 0.01 significance level.

