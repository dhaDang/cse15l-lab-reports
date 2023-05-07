## LAB REPORT 2 <br> Danielle Dang 
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
```
The output was: 


<img width="285" alt="Screen Shot 2023-05-06 at 3 26 51 PM" src="https://user-images.githubusercontent.com/130107069/236648809-8f8e72c7-1cdc-44e5-b4b2-cd41de42dafe.png">

Using the -v option with grep, I was able to find all the lines in the file "1468-6708-3-1.txt" that does not have the pattern "the". This command is great for finding data/information that excludes certain words or patterns. 

Another way I used -v with grep is: 
```
danielle@Danielles-MBP biomed % grep -v health 1468-6708-3-1.txt
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

Here, the option -n acts as a key to tell grep to look into the file "1468-6708-3-1.txt" and kep track of the lines that includes the pattern "death". It would then output the numberline and the actual content of the line that has "death" in it. This is a useful option that can quickly provide information on where a certain phrase/pattern is located. 

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

Here, the option -n or numberline is telling grep to go into the file "1468-6708-3-1.txt" and keep track of the numberline "women" appears as well as the actual content itself in the line. It would then output this information for me in the terminal. This would be useful if I was curious about women's health but didn't want to look through the whole text file. It would be a great reference point as to where information about women's health is in general, while also giving me a peak into the type of information on women's health each line focuses on. 

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
<img width="482" alt="Screen Shot 2023-05-06 at 4 04 16 PM" src="https://user-images.githubusercontent.com/130107069/236649698-6b6493fc-9237-476e-a514-c3c229df445a.png">

