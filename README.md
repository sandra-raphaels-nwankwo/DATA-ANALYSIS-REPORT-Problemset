DATA ANALYSIS REPORT (by Sandra Nwankwo)
1. INTRODUCTION
The issue of student health and well-being has become a pressing concern, capturing national 
attention, and sparking urgent conversations among college and university leaders. This study 
focuses on examining the health and wellness of students enrolled in a liberal arts college at 
Northeastern University in the United States. A sample of 253 college students obtained from their 
liberal arts college in the northeastern United States was used for this study.
The goal of this analysis is to find the average combined depressed, anxious, and stressed college 
students, and ascertain the proportion of college students who engage in the practice of pulling allnighters, a behavior often associated with detrimental effects on sleep quality and overall wellbeing. Throughout this paper, we aim to provide insights for interventions promoting student wellbeing.
2. DATA ANALYSIS
The software used in this data analysis was R. To address the first research question, the dataset 
was first loaded into the software. The str() function was used to find the average combined 
depressed, anxious, and stressed college students. Additionally, the str() function was utilized to 
display the internal structure of the variable, DASscore, in the dataset, SleepStudy. The output of 
this function showed the mean, median, first quartile, third quartile, and range of the variable, 
DASscore. Subsequently, a graphical summary of the variable was created using a histogram, since 
it is numerical data.
To estimate the proportion of college students who pulled all-nighters (AllNighter) in this dataset, 
the prop.table() function was used to obtain this information. For further visualization of this 
variable, a bar plot was created since the data in this variable is categorical. To calculate the interval 
estimates of the two variables at the center of this analysis, we used the prop() function.
3. RESULTS
The histogram revealed a right-skewed distribution of DASscore, centered at 20.04, indicating 
the presence of extreme values. This suggests the presence of extreme values. The analysis of the 
AllNighter variable showed that approximately 86.56% of the students did not pull an all-nighter, 
while approximately 13.44% of the students in the sample pulled an all-nighter. The 95% 
confidence interval for AllNighter was estimated to be 9.61% to 18.41%, and for DASscore, it 
was 61.39% to 73.24%.
3. INFERENCE
The 95% confidence interval for the proportion of college students who pulled all-nighters 
(AllNighter) suggests a significant minority engage in this behavior (9.61% to 18.41%). 
Additionally, for the DASscore variable, the interval estimate (61.39% to 73.24%) indicates that a 
considerable majority of college students exhibit elevated psychological distress.
4. CONCLUSION
The analysis confirms that a significant proportion of students experience elevated psychological 
distress, with a minority engaging in all-nighter practices. While the study provides valuable 
insights, limitations such as sample size and generalizability should be considered in interpreting 
the findings and informing future research and interventions.
APPENDIX
Sandra Nwankwo
2024-02-12
#import dataset
SleepStudy <- read.csv("~/PUBH 6450/Week 4/SleepStudy.csv")
summary(SleepStudy)
5. APPENDIX
## Gender ClassYear LarkOwl NumEarlyClass
## Min. :0.0000 Min. :1.000 Length:253 Min. :0.000
## 1st Qu.:0.0000 1st Qu.:2.000 Class :character 1st Qu.:0.000
## Median :0.0000 Median :2.000 Mode :character Median :2.000
## Mean :0.4032 Mean :2.478 Mean :1.735
## 3rd Qu.:1.0000 3rd Qu.:3.000 3rd Qu.:3.000
## Max. :1.0000 Max. :4.000 Max. :5.000
## EarlyClass GPA ClassesMissed CognitionZscore
## Min. :0.000 Min. :2.000 Min. : 0.000 Min. :-1.62e+00
## 1st Qu.:0.000 1st Qu.:3.000 1st Qu.: 0.000 1st Qu.:-4.80e-01
## Median :1.000 Median :3.300 Median : 1.000 Median :-1.00e-02
## Mean :0.664 Mean :3.244 Mean : 2.209 Mean :-3.95e-05
## 3rd Qu.:1.000 3rd Qu.:3.500 3rd Qu.: 3.000 3rd Qu.: 4.40e-01
## Max. :1.000 Max. :4.000 Max. :20.000 Max. : 1.96e+00
## PoorSleepQuality DepressionScore AnxietyScore StressScore
## Min. : 1.000 Min. : 0.000 Min. : 0.000 Min. : 0.000
## 1st Qu.: 4.000 1st Qu.: 1.000 1st Qu.: 1.000 1st Qu.: 3.000
## Median : 6.000 Median : 3.000 Median : 4.000 Median : 8.000
## Mean : 6.257 Mean : 5.202 Mean : 5.372 Mean : 9.466
## 3rd Qu.: 8.000 3rd Qu.: 7.000 3rd Qu.: 8.000 3rd Qu.:14.000
## Max. :18.000 Max. :35.000 Max. :26.000 Max. :37.000
## DepressionStatus AnxietyStatus Stress DASScore
## Length:253 Length:253 Length:253 Min. : 0.00
## Class :character Class :character Class :character 1st Qu.: 7.00
## Mode :character Mode :character Mode :character Median :16.00
## Mean :20.04
## 3rd Qu.:28.00
## Max. :82.00
## Happiness AlcoholUse Drinks WeekdayBed
## Min. : 0.00 Length:253 Min. : 0.000 Min. :21.80
## 1st Qu.:24.00 Class :character 1st Qu.: 3.000 1st Qu.:24.20
## Median :28.00 Mode :character Median : 5.000 Median :24.80
## Mean :26.11 Mean : 5.569 Mean :24.85
1
## 3rd Qu.:30.00 3rd Qu.: 8.000 3rd Qu.:25.50
## Max. :35.00 Max. :24.000 Max. :29.10
## WeekdayRise WeekdaySleep WeekendBed WeekendRise
## Min. : 5.500 Min. : 3.000 Min. :21.50 Min. : 5.25
## 1st Qu.: 8.000 1st Qu.: 7.200 1st Qu.:24.88 1st Qu.: 9.25
## Median : 8.500 Median : 7.950 Median :25.50 Median :10.25
## Mean : 8.586 Mean : 7.866 Mean :25.58 Mean :10.20
## 3rd Qu.: 9.150 3rd Qu.: 8.600 3rd Qu.:26.25 3rd Qu.:11.00
## Max. :12.020 Max. :10.970 Max. :30.25 Max. :15.00
## WeekendSleep AverageSleep AllNighter
## Min. : 4.000 Min. : 4.950 Min. :0.0000
## 1st Qu.: 7.250 1st Qu.: 7.430 1st Qu.:0.0000
## Median : 8.250 Median : 8.000 Median :0.0000
## Mean : 8.217 Mean : 7.966 Mean :0.1344
## 3rd Qu.: 9.250 3rd Qu.: 8.590 3rd Qu.:0.0000
## Max. :12.750 Max. :10.620 Max. :1.0000
#find mean of DAS Score
summary(SleepStudy$DASScore)
## Min. 1st Qu. Median Mean 3rd Qu. Max.
## 0.00 7.00 16.00 20.04 28.00 82.00
#Create a histogram for DAS score
hist(SleepStudy$DASScore)
Histogram of SleepStudy$DASScore
SleepStudy$DASScore
Frequency
0 20 40 60 80
0 20 40 60 80
2
# What is an estimate for the proportion of college students who pulled all nighters (AllNighter) for this population?
prop.table(table(SleepStudy$AllNighter))
##
## 0 1
## 0.8656126 0.1343874
# Create a bar plot directly with specified colors
barplot(table(SleepStudy$AllNighter),
main = "Bar Plot of AllNighter",
xlab = "AllNighter Status",
ylab = "Frequency",
col = c("skyblue", "salmon"),
legend = c("Did not pull all-nighter", "Pulled all-nighter"),
names.arg = c("No", "Yes"))
No Yes
Did not pull all−nighter
Pulled all−nighter
Bar Plot of AllNighter
AllNighter Status
Frequency
0 50 100 150 200
# Count the number of students who pulled an all-nighter
num_allnighter <- sum(SleepStudy$AllNighter == 1)
# Print the number of students who pulled an all-nighter
cat("Number of students who pulled an all-nighter:", num_allnighter, "\n")
## Number of students who pulled an all-nighter: 34
3
# Calculate interval estimate for ALL NIGHTER
prop.test(34, 253, conf.level=0.95)
##
## 1-sample proportions test with continuity correction
##
## data: 34 out of 253, null probability 0.5
## X-squared = 133.82, df = 1, p-value < 2.2e-16
## alternative hypothesis: true p is not equal to 0.5
## 95 percent confidence interval:
## 0.09609494 0.18412247
## sample estimates:
## p
## 0.1343874
# Define thresholds for depression, anxiety, and stress
thresholds <- c(depression = 10, anxiety = 10, stress = 10)
# Count the number of students meeting each criterion
num_students <- sapply(thresholds, function(threshold) sum(SleepStudy$DASScore >= threshold))
# Print the number of students meeting each criterion
cat("Number of students classified as depressed, anxious, and stressed:", num_students, "\n")
## Number of students classified as depressed, anxious, and stressed: 171 171 171
# Calculate interval estimate for DASscore
prop.test(171, 253, conf.level=0.95)
##
## 1-sample proportions test with continuity correction
##
## data: 171 out of 253, null probability 0.5
## X-squared = 30.609, df = 1, p-value = 3.157e-08
## alternative hypothesis: true p is not equal to 0.5
## 95 percent confidence interval:
## 0.6139226 0.7324159
## sample estimates:
## p
## 0.6758893
4
