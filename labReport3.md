## LAB REPORT 3 <br> Danielle Dang 
<br>

The command I choose to focus on for this lab report is 

```
grep 
```

**What does grep do?**

Grep is a command that searches for a given pattern within files. Furthermore, running grep with a string and a text file will output the lines in the text file that matches the string. 

The general syntax for grep is:

```
grep [option] [pattern] [file]
```

**Some options we can run with grep to manipulate how it matches the pattern and files:**

**1) Using grep to get the amount of times a certain pattern matches the text file contents.**

Using the biomed files in ./technical I was able to run this command: 

```
danielle@Danielles-MBP biomed % grep -c health 1468-6708-3-1.txt
44
```
(with line 1 being input and the following line being the output)

Here the option -c acts as a key to tell grep to count the amount of times a pattern appears in the text file. In this case, the option is telling grep to go into the text file I provided "1468-6708-3-1.txt" and count the amount of times "health" appears, which was 44 times. The grep command is generally helpful for searching through long files or data, however the option -c is useful for the purposes of finding how many times a certain pattern appears rather than the actual lines they appear. 

Another way I used grep with the option count is:
```
danielle@Danielles-MBP biomed % grep -c  12  1468-6708-3-1.txt
1
```
(with line 1 being input and the following line being the output)

Here, the option -c acts as a key to tell grep to count the amount of times "12" shows up in the same text file above. This shows that -c also works with number characters rather than solely alphabethical characters. This option with the grep command is useful for getting quick information on how many times certain numbers or words appear in long data files. 

**2) Using grep the find lines within a file that doesn't match the given pattern**

Using the biomed files in ./technical I was able to run this command: 

```
danielle@Danielles-MBP biomed % grep -v  the  1468-6708-3-1.txt
Introduction
        Older adults are frequently counseled to lose weight,
        even though there is little evidence that overweight is
        associated with increased mortality in those over age 65.
        Six large controlled population-based studies of
        non-smoking older adults have investigated the association
        between body mass index (BMI) and mortality, controlling
        for relevant covariates [ 1 2 3 4 5 6 ] . All studies found
        excess risk for persons with very low BMI, but that persons
        with moderately high BMI had little or no extra risk except
        in certain small subsets. A review of 13 studies of older
        adults drew similar conclusions [ 7 ] .
        throughout adult life. It may be that a small amount of
        gradual weight gain is normative and associated with the
        weight standards be adjusted upwards for age [ 8 ] . Such
        recommendations remain controversial, however, because the
        number of studies of older persons is fairly small, and
        because few studies have examined the relation of BMI to
        elderly [ 9 ] .
        In older adults, risk factors may have a greater effect
        trials of weight modification might be more successful if
        decreased mortality. Clinical trials powered to detect
        differences in YHL would often require fewer subjects than
        trials to detect survival differences or cardiovascular
        events [ 10 ] . In this paper we study whether BMI at
        baseline is associated with living longer, and/or with more
        whom risk factors, subclinical disease, and morbidity are
        well characterized. The goal is to determine whether
        analyses based on years of life (YOL) or on YHL would
        provide substantively different results, and which measure
        would yield more powerful evaluations of weight
        modification interventions in older adults.
      
      
        Materials and methods
        
          Study design: The Cardiovascular Health
          Study
          The Cardiovascular Health Study (CHS) is a
          population-based longitudinal study of 5,888 adults aged
          65 and older at baseline [ 11 ] . Subjects were recruited
          from a random sample of the Medicare eligibility lists in
          four US counties. Extensive baseline data were collected
          for all subjects using a baseline home interview, an
          annual mail questionnaire, and annual clinic
          examinations. Additional information was collected in a
          brief telephone interview 6 months after each scheduled
          visit. Two cohorts were followed, one with 7 years of
          follow-up (n = 5,201) and the second (all African
          American, n = 687) with 4 years of follow-up to date.
          Data collection began in 1989, and follow-up is virtually
          complete for all surviving subjects [ 12 ] .
        
        
          Body mass index
          BMI was calculated as measured weight in kilograms
          divided by the square of measured height in meters. A
          report from the National Heart Lung and Blood Institute
          classifies normal weight (without reference to age) as a
          BMI of 18.5 to 24.9; overweight as 25 to 29.9; and
          obesity as 30.0 and higher [ 13 ] . We consider
          separately the group with BMI between 18.5 and 20, which
          was associated with lower survival in studies cited
          above.
        
        
          YOL is the number of years that a person lived in the
          7 years after baseline. YHL is the number of years in
          or active life expectancy [ 14 ] . We based YHL on
          good, fair, or poor?) (EVGFP) which was collected every 6
          months. EVGFP is a simple but well-known measure, which
          has been studied in detail [ 15 16 ] , and is predictive
          time. We used linear interpolation to estimate missing
          data when there were known values before and after the
          missing value, bringing the percent complete to 95% [ 18
          ] .
          For this analysis we defined YHL as the number of
          years (of 7) in which a person reported excellent, very
          (for persons who were never in excellent, very good, or
          months, YHL has a reasonably continuous distribution. A
          used an alternative approach, which assigns a different
          value to each level of EVGFP [ 19 ] . Preliminary results
          were similar for the two approaches, however, and we
          report results using only the simpler definition.
          The calculations had to be modified to include the 438
          persons in the second African American cohort, who have
          been followed only 4 years to date. For those persons,
          and for 70 persons in the first cohort who did not have
          complete data, we estimated the last 4 years of YOL and
          years, using validated methods presented elsewhere [ 20 ]
          . That article showed that estimated 4-year YOL and YHL
          were unbiased for the African American cohort. In the
          primary analysis we used observed 7-year YOL and YHL when
          they were available, and observed 3-year YOL and YHL plus
          4-year estimated YOL and YHL when they were not (about
          10% of the sample). We performed all analyses with and
          without the persons who had partially estimated data, to
          ensure that the estimation had not distorted the
          findings.
        
        
          Covariates
          The goal is to examine the association of YOL and YHL
          with BMI. To adjust for possible confounding we chose
          baseline covariates that were prevalent in the elderly,
          related to mortality and morbidity in previous studies,
          and likely to be related to BMI. Self-reported covariates
          include age, gender, smoking (never or former), history
          of arthritis, cancer, diabetes, fair or poor self-rated
          or in instrumental activities of daily living, and 10
          pounds or more unintended weight loss in the year before
          baseline. Clinical covariates include hypertension,
          cardiovascular disease (prevalent heart disease,
          peripheral vascular disease, or cerebrovascular disease),
          maximum thickness of the internal carotid artery,
          depression (CESD score), serum albumin, serum
          cholesterol, and serum creatinine. These measures are
          explained in more detail elsewhere [ 21 22 23 24 ] . We
          excluded 697 current smokers and 313 others with
          incomplete covariate data, leaving 4,878 persons on whom
          this analysis is based.
        
        
          Analysis
          All analyses were performed separately for men and
          women. We calculated two sets of adjusted values, as
          follows. We regressed YOL and YHL first on age, age
          squared, race, and smoking history (former or never), and
          second on all of the covariates listed above. We
          calculated adjusted YOL as a person's observed YOL minus
          predicted YOL (from the regression) plus the mean YOL
          (6.52 years for women or 6.06 for men). That is, a
          person's adjusted YOL is his residual from the regression
          plus the grand mean. The mean of this new variable, for a
          group of subjects, is the adjusted mean YOL for that
          group. Adjusted YHL was calculated in a similar manner.
          We calculated two sets of adjusted variables because of
          the possibility of 'over-adjustment', controlling
          inappropriately for factors (such as diabetes) which may
          have been causally affected by the person's weight. We
          plotted mean adjusted YOL and YHL against BMI, and tested
          for difference among BMI groups using confidence
          intervals or analysis of variance. Finally we calculated
          the effect size for each measure, comparing each BMI
          subgroup to the 'normal' group. The effect size is the
          difference in mean YOL (or YHL) in two groups divided by
          their common standard deviation. Since the sample size
          required to detect an effect of this magnitude is
          proportional to the inverse of the squared effect size,
          large effect sizes are desirable.
        
      
      
        Results
        Table 1shows the distribution of key variables by sex
        and race. Mean age at baseline was 73.1 and about two
        thirds of the men and a third of the women were former
        smokers. Black women had a higher mean BMI and higher
        percent obese (BMI ≥ 30) than the other three groups. Black
        men were most likely to have unintentionally lost more than
        10 pounds in the past year; white women were least
        likely.
        declining to 57% at the end of 7 years; 20% had died (data
        thus substantial change in EVGFP over time, in both
        directions. Table 1shows the mean YOL and YHL (calculated
        from EVGFP) in the first seven years of the study, adjusted
        to age 73. For example, black women averaged 6.3 YOL, but
        only 4.2 YHL of a maximum possible 7. We calculated some
        additional descriptive statistics, shown in the final two
        lost to death (7 minus YOL). White women had the most YHL
        and black men the fewest; black women had the most years of
        the most years to death (1.3 out of 7) while white women
        lost only 0.4 years. For blacks, about 68% of their YOL
        Among whites, the gender differences in Table 1were
        statistically significant (p <.05) except for BMI and
        unintended weight loss. Among blacks, gender differences
        were significant except for 10 pounds unintended weight
        loss and weight loss since age 50. Among males, there were
        significant differences between black and white for BMI,
        and years lost to death. Whites in the sample had higher
        income and education (data not shown). After adjusting for
        income and education, as well as age and former smoking,
        the difference in BMI was no longer statistically
        significant. Among females, blacks and whites differed
        significantly on BMI, BMI>30, weight loss since age 50,
        After adjustment for income and education, the difference
        in weight loss since age 50 was no longer significant.
        Blacks had significantly lower YOL and YHL than whites
        after adjustment for age, but the difference disappeared
        baseline covariates (analyses not shown).
        We next examined the relationship of BMI to YOL and YHL.
        Table 2presents the mean values of YOL and YHL, adjusted
        for age, race, and previous smoking (columns 1 and 3), and
        also adjusted for the entire set of covariates (columns 2
        and 4). For example, YOL for women, adjusted for age, race,
        and smoking, averaged 6.0 years for women with a baseline
        BMI below 18.5, but averaged 6.6 years for women with a BMI
        from 25 to 29.9. The second column, which shows results
        adjusted for all covariates, is not very different (the
        only discrepancy is for men with BMI < 18.5, a category
        containing only 14 men). Adjustment for extensive
        covariates also made little difference for YHL (columns 3
        and 4). Subsequent analyses are adjusted only for age,
        race, and former smoking. As mentioned above, the group
        with BMI from 18.5 to 20 would be considered 'normal' by
        the NHLBI guidelines, but had lower YOL and YHL than those
        with 20-24.9 in all comparisons. For this reason, and to
        increase sample size for those with low BMI, we combined
        the two lower categories, defining underweight as a BMI
        under 20.
        Figure 1is a plot of adjusted YOL and YHL by sex and
        BMI. For each BMI category the mean and its 95% confidence
        interval are plotted. Categories whose confidence intervals
        do not overlap, or overlap only slightly, are significantly
        different. The bars are slightly offset to permit all error
        bars to be seen.
        YOL for women (the uppermost curve on Figure 1) averaged
        about 6.5 out of 7 years, and showed no evident association
        between BMI and YOL for BMI above 20. Underweight women
        averaged about .25 fewer YOL than other women (p < .05
        compared with normal group). Underweight men also had lower
        YOL, but this group was not significantly different from
        the normal group, in part because of low sample size. Men
        classified as normal, overweight or obese all had about the
        same YOL.
        The lowermost two lines in Figure 1show mean YHL for
        women and men. Women who were normal or overweight averaged
        about 4.9 YHL. The YHL for underweight or obese women was
        about 4.5 years, which was significantly lower than the
        normal group. The relationship of BMI to YHL for men is
        similar, but differences among BMI groups were not
        statistically significant. YHL was significantly higher for
        women than for men in the normal and overweight groups, but
        the sexes had similar YHL in the underweight and obese
        groups.
        We next present the effect size for comparing each group
        to the normal BMI group. The effect sizes are shown in
        Table 3, with the significance results of the associated
        t-tests for the differences in means of the two groups
        being compared. For example, underweight women averaged
        4.50 YHL compared to 4.92 for normal women, and the common
        standard deviation was 1.44. The effect size is thus
        (4.92-4.50)/1.44 = .29. The two groups had significantly
        different YHL, implying that the effect size is also
        significantly greater than zero. A clinical trial of a
        treatment to help underweight women achieve normal weight
        (presumably by addressing the underlying cause) could be
        expected to have 80% power with N = (1.96+.84) 2/.29 2=
        about 93 women per treatment arm, if 7-year YHL were the
        outcome measure.
        The biggest effect sizes are in the first row, comparing
        underweight to normal. YHL and YOL have similar effect
        sizes for women, and are significantly different from zero.
        The effect sizes are not significantly different from zero
        for men, in part because there were only 42 men in the
        underweight category. The effect size comparing overweight
        to normal yielded small, non-significant effect sizes, with
        inconsistent signs, suggesting extremely large sample sizes
        would be needed. For comparing obese to normal, only YHL
        for women showed a large and significant effect size. Thus,
        to that of their normal weight peers could be performed
        using either YHL or YOL as the outcome variable. Trials to
        make obese women comparable to normal women could be
        evaluated using YHL, but not YOL. Trials to improve the
        probably be fruitless since there is no evidence that being
        overweight (for men or women) or obese (for men) affects
        YOL or YHL.
        As mentioned above, we repeated these analyses excluding
        the persons with partially estimated data, and using two
        different ways of coding YHL. The only substantive change
        was that some of the differences between blacks and whites
        shown in Table 1were no longer statistically significant,
        due to a smaller sample size.
      
      
        Discussion
        
          Optimal weight and overweight
          Recent studies have defined obesity without reference
          to age [ 6 13 30 ] . Andres 
          et al proposed a desirable BMI of
          24-30 for persons aged 60 to 69 [ 8 ] . Allison 
          et al [ 31 ] proposed 27-30 for
          older men and 30-35 for older women. In Figure 1, the
          overweight (as opposed to the obese) are no different
          from those of normal weight, suggesting that these two
          categories could be combined for older adults. Since
          future improvements in life expectancy may be limited [
          32 ] , the greatest advances may be made by improving
          people's YHL. This suggests that the development of
          future guidelines should take YHL or other measures of
          quality of life into account.
        
        
          Implications for clinical trials
          Based on these findings, trials to address obesity in
          older women could be efficient if YHL (but not YOL) was
          the outcome measure. That is, women who changed from
          being obese to being normal would likely show changes in
          YHL, but not YOL. Clinical trials of weight modification
          interventions for older adults who were merely overweight
          would appear to be fruitless since the interventions
          would probably not have a direct effect on either YOL or
          YHL.
          Weight or weight change are sometimes used as the
          outcome in evaluations of interventions such as diet or
          exercise programs. The fact that weight is not associated
          evaluations should be considered critically when older
          adults are the subjects. This is particularly important
          in the light of recent findings, which found that
          interventions such as weight-loss drugs may be harmful [
          33 34 ] . For older adults, the risks associated with
          higher weight are especially unclear, and the optimal
          outcome for a trial of weight loss in older adults
          mortality.
          found for underweight older adults. Clinical trials whose
          normal-weight peers (presumably by addressing the
          underlying conditions that caused the low weight) could
          be performed efficiently using either YOL or YHL as the
          outcome measure. Both YOL and YHL would be clinically
          significant in this patient group.
        
        
          Potential limitations
          average older adult; however, adjustment for detailed
          covariates made little difference in the findings. We
          10% of the sample, but results with and without this
          group were similar. Analysis of mean YOL instead of the
          more traditional survival analysis survival analysis was
          appropriate here, since virtually no persons were lost to
          follow-up. Biases caused by over-adjustment are probably
          not large, since the findings were not sensitive to the
          number of variables adjusted for.
          These results are for a 7-year follow-up. The relative
          superiority of YHL to YOL would probably hold in trials
          with shorter follow-up. The effect sizes in Table 3might
          also be appropriate in shorter trials, since lengthy
          trials often add little information [ 10 ] .
          EVGFP, on which YHL was based, might have missed some
          person who is depressed because of a poor self-image
          related to obesity or who has osteo-arthritis related to
          obesity and limits to activities to successfully avoid
          pain would surely have worse EVGFP than others, based on
          designed specifically to measure those conditions might
          be more sensitive to change in weight than EVGFP. If YHL
          were based on such measures, the superiority of YHL to
          YOL would likely be even greater than that shown here.
          These more sensitive measures might also have detected
          differences between the overweight and normal weight
          persons, but we think this is unlikely given the absence
          of any differences in EVGFP.
        
      
      
        Conclusion
        Recommendations for desirable weight have been
        found associations between YHL and obesity that were not
        present in the mortality analysis, suggesting that YHL may
        be a more sensitive measure of the burden of obesity in
        older adults, especially for women. Future efforts to
        determine desirable weight guidelines should include
        measures of YHL. Using either YOL or YHL, however, we found
        no excess risk for older adults who would be classified as
        'overweight' by the NHLBI guidelines. This suggests using
        YHL as the outcome measure in clinical trials involving
        obese or underweight older adults, and discouraging trials
        that address older adults who are merely overweight.
      
      
        Competing interests
        None declared
      
      
        Abbreviations
        BMI Body mass index
        CESD Center for Epidemiologic Studies Depression
        Scale
        CHS Cardiovascular Health Study
        poor?
        QALY Quality-adjusted life years
        YOL Years of life
```
The output was: 


<img width="285" alt="Screen Shot 2023-05-06 at 3 26 51 PM" src="https://user-images.githubusercontent.com/130107069/236648809-8f8e72c7-1cdc-44e5-b4b2-cd41de42dafe.png">

Using the -v option with grep, I was able to find all the lines in the file "1468-6708-3-1.txt" that does not have the pattern "the". This command is great for finding data/information that excludes certain words or patterns. 

Another way I used -v with grep is: 
```
danielle@Danielles-MBP biomed % grep -v health 1468-6708-3-1.txt
Introduction
        Older adults are frequently counseled to lose weight,
        even though there is little evidence that overweight is
        associated with increased mortality in those over age 65.
        Six large controlled population-based studies of
        non-smoking older adults have investigated the association
        between body mass index (BMI) and mortality, controlling
        for relevant covariates [ 1 2 3 4 5 6 ] . All studies found
        excess risk for persons with very low BMI, but that persons
        with moderately high BMI had little or no extra risk except
        in certain small subsets. A review of 13 studies of older
        adults drew similar conclusions [ 7 ] .
        throughout adult life. It may be that a small amount of
        gradual weight gain is normative and associated with the
        weight standards be adjusted upwards for age [ 8 ] . Such
        recommendations remain controversial, however, because the
        number of studies of older persons is fairly small, and
        because few studies have examined the relation of BMI to
        elderly [ 9 ] .
        In older adults, risk factors may have a greater effect
        trials of weight modification might be more successful if
        decreased mortality. Clinical trials powered to detect
        differences in YHL would often require fewer subjects than
        trials to detect survival differences or cardiovascular
        events [ 10 ] . In this paper we study whether BMI at
        baseline is associated with living longer, and/or with more
        whom risk factors, subclinical disease, and morbidity are
        well characterized. The goal is to determine whether
        analyses based on years of life (YOL) or on YHL would
        provide substantively different results, and which measure
        would yield more powerful evaluations of weight
        modification interventions in older adults.
      
      
        Materials and methods
        
          Study design: The Cardiovascular Health
          Study
          The Cardiovascular Health Study (CHS) is a
          population-based longitudinal study of 5,888 adults aged
          65 and older at baseline [ 11 ] . Subjects were recruited
          from a random sample of the Medicare eligibility lists in
          four US counties. Extensive baseline data were collected
          for all subjects using a baseline home interview, an
          annual mail questionnaire, and annual clinic
          examinations. Additional information was collected in a
          brief telephone interview 6 months after each scheduled
          visit. Two cohorts were followed, one with 7 years of
          follow-up (n = 5,201) and the second (all African
          American, n = 687) with 4 years of follow-up to date.
          Data collection began in 1989, and follow-up is virtually
          complete for all surviving subjects [ 12 ] .
        
        
          Body mass index
          BMI was calculated as measured weight in kilograms
          divided by the square of measured height in meters. A
          report from the National Heart Lung and Blood Institute
          classifies normal weight (without reference to age) as a
          BMI of 18.5 to 24.9; overweight as 25 to 29.9; and
          obesity as 30.0 and higher [ 13 ] . We consider
          separately the group with BMI between 18.5 and 20, which
          was associated with lower survival in studies cited
          above.
        
        
          YOL is the number of years that a person lived in the
          7 years after baseline. YHL is the number of years in
          or active life expectancy [ 14 ] . We based YHL on
          good, fair, or poor?) (EVGFP) which was collected every 6
          months. EVGFP is a simple but well-known measure, which
          has been studied in detail [ 15 16 ] , and is predictive
          time. We used linear interpolation to estimate missing
          data when there were known values before and after the
          missing value, bringing the percent complete to 95% [ 18
          ] .
          For this analysis we defined YHL as the number of
          years (of 7) in which a person reported excellent, very
          (for persons who were never in excellent, very good, or
          months, YHL has a reasonably continuous distribution. A
          used an alternative approach, which assigns a different
          value to each level of EVGFP [ 19 ] . Preliminary results
          were similar for the two approaches, however, and we
          report results using only the simpler definition.
          The calculations had to be modified to include the 438
          persons in the second African American cohort, who have
          been followed only 4 years to date. For those persons,
          and for 70 persons in the first cohort who did not have
          complete data, we estimated the last 4 years of YOL and
          years, using validated methods presented elsewhere [ 20 ]
          . That article showed that estimated 4-year YOL and YHL
          were unbiased for the African American cohort. In the
          primary analysis we used observed 7-year YOL and YHL when
          they were available, and observed 3-year YOL and YHL plus
          4-year estimated YOL and YHL when they were not (about
          10% of the sample). We performed all analyses with and
          without the persons who had partially estimated data, to
          ensure that the estimation had not distorted the
          findings.
        
        
          Covariates
          The goal is to examine the association of YOL and YHL
          with BMI. To adjust for possible confounding we chose
          baseline covariates that were prevalent in the elderly,
          related to mortality and morbidity in previous studies,
          and likely to be related to BMI. Self-reported covariates
          include age, gender, smoking (never or former), history
          of arthritis, cancer, diabetes, fair or poor self-rated
          or in instrumental activities of daily living, and 10
          pounds or more unintended weight loss in the year before
          baseline. Clinical covariates include hypertension,
          cardiovascular disease (prevalent heart disease,
          peripheral vascular disease, or cerebrovascular disease),
          maximum thickness of the internal carotid artery,
          depression (CESD score), serum albumin, serum
          cholesterol, and serum creatinine. These measures are
          explained in more detail elsewhere [ 21 22 23 24 ] . We
          excluded 697 current smokers and 313 others with
          incomplete covariate data, leaving 4,878 persons on whom
          this analysis is based.
        
        
          Analysis
          All analyses were performed separately for men and
          women. We calculated two sets of adjusted values, as
          follows. We regressed YOL and YHL first on age, age
          squared, race, and smoking history (former or never), and
          second on all of the covariates listed above. We
          calculated adjusted YOL as a person's observed YOL minus
          predicted YOL (from the regression) plus the mean YOL
          (6.52 years for women or 6.06 for men). That is, a
          person's adjusted YOL is his residual from the regression
          plus the grand mean. The mean of this new variable, for a
          group of subjects, is the adjusted mean YOL for that
          group. Adjusted YHL was calculated in a similar manner.
          We calculated two sets of adjusted variables because of
          the possibility of 'over-adjustment', controlling
          inappropriately for factors (such as diabetes) which may
          have been causally affected by the person's weight. We
          plotted mean adjusted YOL and YHL against BMI, and tested
          for difference among BMI groups using confidence
          intervals or analysis of variance. Finally we calculated
          the effect size for each measure, comparing each BMI
          subgroup to the 'normal' group. The effect size is the
          difference in mean YOL (or YHL) in two groups divided by
          their common standard deviation. Since the sample size
          required to detect an effect of this magnitude is
          proportional to the inverse of the squared effect size,
          large effect sizes are desirable.
        
      
      
        Results
        Table 1shows the distribution of key variables by sex
        and race. Mean age at baseline was 73.1 and about two
        thirds of the men and a third of the women were former
        smokers. Black women had a higher mean BMI and higher
        percent obese (BMI ≥ 30) than the other three groups. Black
        men were most likely to have unintentionally lost more than
        10 pounds in the past year; white women were least
        likely.
        declining to 57% at the end of 7 years; 20% had died (data
        thus substantial change in EVGFP over time, in both
        directions. Table 1shows the mean YOL and YHL (calculated
        from EVGFP) in the first seven years of the study, adjusted
        to age 73. For example, black women averaged 6.3 YOL, but
        only 4.2 YHL of a maximum possible 7. We calculated some
        additional descriptive statistics, shown in the final two
        lost to death (7 minus YOL). White women had the most YHL
        and black men the fewest; black women had the most years of
        the most years to death (1.3 out of 7) while white women
        lost only 0.4 years. For blacks, about 68% of their YOL
        Among whites, the gender differences in Table 1were
        statistically significant (p <.05) except for BMI and
        unintended weight loss. Among blacks, gender differences
        were significant except for 10 pounds unintended weight
        loss and weight loss since age 50. Among males, there were
        significant differences between black and white for BMI,
        and years lost to death. Whites in the sample had higher
        income and education (data not shown). After adjusting for
        income and education, as well as age and former smoking,
        the difference in BMI was no longer statistically
        significant. Among females, blacks and whites differed
        significantly on BMI, BMI>30, weight loss since age 50,
        After adjustment for income and education, the difference
        in weight loss since age 50 was no longer significant.
        Blacks had significantly lower YOL and YHL than whites
        after adjustment for age, but the difference disappeared
        baseline covariates (analyses not shown).
        We next examined the relationship of BMI to YOL and YHL.
        Table 2presents the mean values of YOL and YHL, adjusted
        for age, race, and previous smoking (columns 1 and 3), and
        also adjusted for the entire set of covariates (columns 2
        and 4). For example, YOL for women, adjusted for age, race,
        and smoking, averaged 6.0 years for women with a baseline
        BMI below 18.5, but averaged 6.6 years for women with a BMI
        from 25 to 29.9. The second column, which shows results
        adjusted for all covariates, is not very different (the
        only discrepancy is for men with BMI < 18.5, a category
        containing only 14 men). Adjustment for extensive
        covariates also made little difference for YHL (columns 3
        and 4). Subsequent analyses are adjusted only for age,
        race, and former smoking. As mentioned above, the group
        with BMI from 18.5 to 20 would be considered 'normal' by
        the NHLBI guidelines, but had lower YOL and YHL than those
        with 20-24.9 in all comparisons. For this reason, and to
        increase sample size for those with low BMI, we combined
        the two lower categories, defining underweight as a BMI
        under 20.
        Figure 1is a plot of adjusted YOL and YHL by sex and
        BMI. For each BMI category the mean and its 95% confidence
        interval are plotted. Categories whose confidence intervals
        do not overlap, or overlap only slightly, are significantly
        different. The bars are slightly offset to permit all error
        bars to be seen.
        YOL for women (the uppermost curve on Figure 1) averaged
        about 6.5 out of 7 years, and showed no evident association
        between BMI and YOL for BMI above 20. Underweight women
        averaged about .25 fewer YOL than other women (p < .05
        compared with normal group). Underweight men also had lower
        YOL, but this group was not significantly different from
        the normal group, in part because of low sample size. Men
        classified as normal, overweight or obese all had about the
        same YOL.
        The lowermost two lines in Figure 1show mean YHL for
        women and men. Women who were normal or overweight averaged
        about 4.9 YHL. The YHL for underweight or obese women was
        about 4.5 years, which was significantly lower than the
        normal group. The relationship of BMI to YHL for men is
        similar, but differences among BMI groups were not
        statistically significant. YHL was significantly higher for
        women than for men in the normal and overweight groups, but
        the sexes had similar YHL in the underweight and obese
        groups.
        We next present the effect size for comparing each group
        to the normal BMI group. The effect sizes are shown in
        Table 3, with the significance results of the associated
        t-tests for the differences in means of the two groups
        being compared. For example, underweight women averaged
        4.50 YHL compared to 4.92 for normal women, and the common
        standard deviation was 1.44. The effect size is thus
        (4.92-4.50)/1.44 = .29. The two groups had significantly
        different YHL, implying that the effect size is also
        significantly greater than zero. A clinical trial of a
        treatment to help underweight women achieve normal weight
        (presumably by addressing the underlying cause) could be
        expected to have 80% power with N = (1.96+.84) 2/.29 2=
        about 93 women per treatment arm, if 7-year YHL were the
        outcome measure.
        The biggest effect sizes are in the first row, comparing
        underweight to normal. YHL and YOL have similar effect
        sizes for women, and are significantly different from zero.
        The effect sizes are not significantly different from zero
        for men, in part because there were only 42 men in the
        underweight category. The effect size comparing overweight
        to normal yielded small, non-significant effect sizes, with
        inconsistent signs, suggesting extremely large sample sizes
        would be needed. For comparing obese to normal, only YHL
        for women showed a large and significant effect size. Thus,
        to that of their normal weight peers could be performed
        using either YHL or YOL as the outcome variable. Trials to
        make obese women comparable to normal women could be
        evaluated using YHL, but not YOL. Trials to improve the
        probably be fruitless since there is no evidence that being
        overweight (for men or women) or obese (for men) affects
        YOL or YHL.
        As mentioned above, we repeated these analyses excluding
        the persons with partially estimated data, and using two
        different ways of coding YHL. The only substantive change
        was that some of the differences between blacks and whites
        shown in Table 1were no longer statistically significant,
        due to a smaller sample size.
      
      
        Discussion
        
          Optimal weight and overweight
          Recent studies have defined obesity without reference
          to age [ 6 13 30 ] . Andres 
          et al proposed a desirable BMI of
          24-30 for persons aged 60 to 69 [ 8 ] . Allison 
          et al [ 31 ] proposed 27-30 for
          older men and 30-35 for older women. In Figure 1, the
          overweight (as opposed to the obese) are no different
          from those of normal weight, suggesting that these two
          categories could be combined for older adults. Since
          future improvements in life expectancy may be limited [
          32 ] , the greatest advances may be made by improving
          people's YHL. This suggests that the development of
          future guidelines should take YHL or other measures of
          quality of life into account.
        
        
          Implications for clinical trials
          Based on these findings, trials to address obesity in
          older women could be efficient if YHL (but not YOL) was
          the outcome measure. That is, women who changed from
          being obese to being normal would likely show changes in
          YHL, but not YOL. Clinical trials of weight modification
          interventions for older adults who were merely overweight
          would appear to be fruitless since the interventions
          would probably not have a direct effect on either YOL or
          YHL.
          Weight or weight change are sometimes used as the
          outcome in evaluations of interventions such as diet or
          exercise programs. The fact that weight is not associated
          evaluations should be considered critically when older
          adults are the subjects. This is particularly important
          in the light of recent findings, which found that
          interventions such as weight-loss drugs may be harmful [
          33 34 ] . For older adults, the risks associated with
          higher weight are especially unclear, and the optimal
          outcome for a trial of weight loss in older adults
          mortality.
          found for underweight older adults. Clinical trials whose
          normal-weight peers (presumably by addressing the
          underlying conditions that caused the low weight) could
          be performed efficiently using either YOL or YHL as the
          outcome measure. Both YOL and YHL would be clinically
          significant in this patient group.
        
        
          Potential limitations
          average older adult; however, adjustment for detailed
          covariates made little difference in the findings. We
          10% of the sample, but results with and without this
          group were similar. Analysis of mean YOL instead of the
          more traditional survival analysis survival analysis was
          appropriate here, since virtually no persons were lost to
          follow-up. Biases caused by over-adjustment are probably
          not large, since the findings were not sensitive to the
          number of variables adjusted for.
          These results are for a 7-year follow-up. The relative
          superiority of YHL to YOL would probably hold in trials
          with shorter follow-up. The effect sizes in Table 3might
          also be appropriate in shorter trials, since lengthy
          trials often add little information [ 10 ] .
          EVGFP, on which YHL was based, might have missed some
          person who is depressed because of a poor self-image
          related to obesity or who has osteo-arthritis related to
          obesity and limits to activities to successfully avoid
          pain would surely have worse EVGFP than others, based on
          designed specifically to measure those conditions might
          be more sensitive to change in weight than EVGFP. If YHL
          were based on such measures, the superiority of YHL to
          YOL would likely be even greater than that shown here.
          These more sensitive measures might also have detected
          differences between the overweight and normal weight
          persons, but we think this is unlikely given the absence
          of any differences in EVGFP.
        
      
      
        Conclusion
        Recommendations for desirable weight have been
        found associations between YHL and obesity that were not
        present in the mortality analysis, suggesting that YHL may
        be a more sensitive measure of the burden of obesity in
        older adults, especially for women. Future efforts to
        determine desirable weight guidelines should include
        measures of YHL. Using either YOL or YHL, however, we found
        no excess risk for older adults who would be classified as
        'overweight' by the NHLBI guidelines. This suggests using
        YHL as the outcome measure in clinical trials involving
        obese or underweight older adults, and discouraging trials
        that address older adults who are merely overweight.
      
      
        Competing interests
        None declared
      
      
        Abbreviations
        BMI Body mass index
        CESD Center for Epidemiologic Studies Depression
        Scale
        CHS Cardiovascular Health Study
        poor?
        QALY Quality-adjusted life years
        YOL Years of life
```
The output was:


<img width="383" alt="Screen Shot 2023-05-06 at 3 31 33 PM" src="https://user-images.githubusercontent.com/130107069/236648935-6d06d7cb-05f2-4512-8fb5-b313357012bf.png">

Using the -v option with grep, I was able to get all the lines in the file "1468-6708-3-1.txt" that doesnt have the word "health" in it. Here, grep is taking the file "1468-6708-3-1.txt" and avoiding all the lines that has a match with "health". This would be useful if I was looking for lines that didn't directly mention health.

**3) Using grep to keep track of the line number of the corresponding line that matches a given pattern**

Using the biomed files in ./technical I was able to run this command: 

```
danielle@Danielles-MBP biomed % grep -n death 1468-6708-3-1.txt 
103:          death, since all are considered 'not healthy'. We also
199:        lost to death (7 minus YOL). White women had the most YHL
202:        the most years to death (1.3 out of 7) while white women
213:        and years lost to death. Whites in the sample had higher
219:        YOL, YHL, years of unhealthy life, and years lost to death.
```
(with line 1 being input and the following line being the output)

Here, the option -n acts as a key to tell grep to look into the file "1468-6708-3-1.txt" and keep track of the lines that includes the pattern "death". It would then output the numberline and the actual content of the line that has "death" in it. This is a useful option that can quickly provide information on where a certain phrase/pattern is located. 

Another way I used grep with the option numberline is:

```
danielle@Danielles-MBP biomed % grep -n women  1468-6708-3-1.txt
151:          women. We calculated two sets of adjusted values, as
157:          (6.52 years for women or 6.06 for men). That is, a
182:        thirds of the men and a third of the women were former
183:        smokers. Black women had a higher mean BMI and higher
186:        10 pounds in the past year; white women were least
195:        to age 73. For example, black women averaged 6.3 YOL, but
199:        lost to death (7 minus YOL). White women had the most YHL
200:        and black men the fewest; black women had the most years of
202:        the most years to death (1.3 out of 7) while white women
230:        and 4). For example, YOL for women, adjusted for age, race,
231:        and smoking, averaged 6.0 years for women with a baseline
232:        BMI below 18.5, but averaged 6.6 years for women with a BMI
252:        YOL for women (the uppermost curve on Figure 1) averaged
254:        between BMI and YOL for BMI above 20. Underweight women
255:        averaged about .25 fewer YOL than other women (p < .05
262:        women and men. Women who were normal or overweight averaged
263:        about 4.9 YHL. The YHL for underweight or obese women was
268:        women than for men in the normal and overweight groups, but
275:        being compared. For example, underweight women averaged
276:        4.50 YHL compared to 4.92 for normal women, and the common
281:        treatment to help underweight women achieve normal weight
284:        about 93 women per treatment arm, if 7-year YHL were the
288:        sizes for women, and are significantly different from zero.
295:        for women showed a large and significant effect size. Thus,
296:        an intervention to improve the health of underweight women
299:        make obese women comparable to normal women could be
303:        overweight (for men or women) or obese (for men) affects
321:          older men and 30-35 for older women. In Figure 1, the
334:          older women could be efficient if YHL (but not YOL) was
335:          the outcome measure. That is, women who changed from
406:        older adults, especially for women. Future efforts to
```
(with line one being the input and the following lines the output) 

Here, the option -n or numberline is telling grep to go into the file "1468-6708-3-1.txt" and keep track of the numberline "women" appears as well as the actual content itself in the line. It would then output this information for me in the terminal. This would be useful if I was curious about women's health but didn't want to look through the whole text file. It would be a great reference point as to where information about women's health is in general, while also giving me a peek into the type of information on women's health each line focuses on. 

**4) Using grep to find whole words that exactly matches a pattern rather than words that partially matches it**

Grep can be a useful tool to find patterns within large files, however the command itself will output anything that might contain a pattern, rather than lines that matches the whole pattern itself. For example using grep with "a" can not only output matches with "a" but also anything that has "a" within it itself, like "apple". 

The option -w or word-regexp can be a useful way to get specific matches and decrease the amount of data grep outputs. 

One way I used grep with -w is:
```
danielle@Danielles-MBP biomed % grep -w future 1468-6708-3-1.txt
          future improvements in life expectancy may be limited [
          future guidelines should take YHL or other measures of
          effects of obesity on risk factors for future health. A
```

(with line one being the input and the following lines the output)

Here, -w is telling grep to look into "1468-6708-3-1.txt" and only return lines that matches the whole pattern "future" rather than partially. This is a useful way to get specific and detailed matches in files with a lot of data. 

Another way I used grep with -w is:
```
danielle@Danielles-MBP biomed % grep -w a 1468-6708-3-1.txt
        throughout adult life. It may be that a small amount of
        In older adults, risk factors may have a greater effect
        years of being healthy, in a cohort of older adults for
          The Cardiovascular Health Study (CHS) is a
          from a random sample of the Medicare eligibility lists in
          for all subjects using a baseline home interview, an
          examinations. Additional information was collected in a
          classifies normal weight (without reference to age) as a
          YOL is the number of years that a person lived in the
          months. EVGFP is a simple but well-known measure, which
          examining health status over time, we added a sixth
          years (of 7) in which a person reported excellent, very
          months, YHL has a reasonably continuous distribution. A
          used an alternative approach, which assigns a different
          calculated adjusted YOL as a person's observed YOL minus
          (6.52 years for women or 6.06 for men). That is, a
          plus the grand mean. The mean of this new variable, for a
          group. Adjusted YHL was calculated in a similar manner.
        thirds of the men and a third of the women were former
        smokers. Black women had a higher mean BMI and higher
        only 4.2 YHL of a maximum possible 7. We calculated some
        and smoking, averaged 6.0 years for women with a baseline
        BMI below 18.5, but averaged 6.6 years for women with a BMI
        only discrepancy is for men with BMI < 18.5, a category
        the two lower categories, defining underweight as a BMI
        Figure 1is a plot of adjusted YOL and YHL by sex and
        significantly greater than zero. A clinical trial of a
        for women showed a large and significant effect size. Thus,
        due to a smaller sample size.
          et al proposed a desirable BMI of
          would probably not have a direct effect on either YOL or
          in a consistent way with health suggests that such
          outcome for a trial of weight loss in older adults
          These results are for a 7-year follow-up. The relative
          person who is depressed because of a poor self-image
        be a more sensitive measure of the burden of obesity in
```
(with line one being the input and the following lines the output)

Here, -w is telling grep to go into the file "1468-6708-3-1.txt" and only output the lines that have "a" by itself, rather than output all the lines that has a word with "a" in it like "calculations". In other words, it outputs lines with "a" by itself rather that all the lines that has words with "a" within it. This helps minimize the amount of lines that would be outputted otherwise without -w and generally helps me sort through a large text file. 

**sources:**
chat gbt!
I used chat gbt (https://chat.openai.com/) and asked it for any useful and interesting grep options for inspiration. 
The prompt I gave it was "hello! Can I have some useful grep commands" (Please see the page below for the prompt I gave it and the output it created for me!) 

<img width="400" alt="Screen Shot 2023-05-18 at 1 17 36 PM" src="https://github.com/dhaDang/cse15l-lab-reports/assets/130107069/74b70257-3059-4b9c-be7a-491fef9aacfa">

I was able to derive the commands and a little understanding of what each does, and from there I applied it to the files in ./technical and see the commands in action! This helped me further understand what each command does and think of ways they would all individually be useful in certain circumstances.  
