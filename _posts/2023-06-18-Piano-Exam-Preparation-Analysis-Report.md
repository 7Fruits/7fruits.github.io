---
published: true
---
My son is going to have the RCM level 7 exam soon. He was supposed to prepare his techniques well if he followed the instruction from his piano teacher. However, the result seems not as expected. Let me help him to practice efficiently through the data analytics result.

#### Target
1. What is his weakest technique? 

2. Is it true that the arpeggios is the most unfamiliar ?

3. Is there any relevance between the page order and the familiarity of the techniques. The order of the techniques are Scales, Chords, then Arpeggios. I assume that he always started from the first page of the book to practice. I think he didn’t spend enough time on the Arpeggios.

#### Steps
1. Collect the data points
2. Update to the excel 
3. Start the data manipulation
4. Work out the data result

I worked with my son for 4 days to go through all the techniques, and I recorded his performance in a form from his book. I graded his playing as below:

|Score|Definition                                           |
|:--|:-----------------------------------------------------:|
|5  |Fluent and accurate without restarting.                |
|4  |Fluent and accurate but with restarting once.          |
|3  |Generally correct notes, but with restarting and pause.|
|2  |Skip this grade to make it as simple as possible.      |
|1  |Skip this grade to make it as simple as possible.      |
|0  |Totally forget the piece and don’t know how to play    |


The techniques have 3 main categories: Scales, Chords, and Arpeggios.  Under each category, there are related items that need to be practiced, 69 techniques in total need to be memorized ！ It’s not easy. That’s why I need the data to help him work smart. The example of the techniques in the excel is as: 

![]({{site.baseurl}}/images/TechniqueList.png)


I input the scores from Jun 2nd to Jun 7th, then calculated the day-by-day average score. I sort and rank the scores to find the techinques with the lowest scores in the column Attention, I could get top 10 lowest scores. See another article about how to rank without gap...
Also I achieved my first result about which technique is the weakest: Chords Leading-Tone Diminished 7th F Minor Broken.

![]({{site.baseurl}}/images/C_RCM7_Tech_Tracking.jpg)


To find the result of the second assumption if it's true the arpeggios are the most unfamiliar, I calculated the overall average score for all the techniques which is 4.26. Then I could find out the percentage of each technique category above and below the average score percentage. From the stacked chart, the Scales group has the best performance, 79% of this group are above the average score which is the highest among other 2 groups Arpeggios and Chords.  It proves the 2nd assumption that the Arpeggios are the most unfamiliar part of the techniques.

![]({{site.baseurl}}/images/TechiqueGroupsPerformance.png)


How about the 3rd assumption? I calculated the average score of the techniques on each page, then I displayed them on the scatter chart with a trendline. From the trendline, I could find the slope of the trendline is gradually getting smaller from the pages of Scales toward the pages of Arpeggios which means the average score of each page is getting lower gradually. So, it could prove the Arpeggios are the weakest techniques and the order of the page impacts the familiarity of the techniques.

![]({{site.baseurl}}/images/PageOrderandTechFamilarity.png)


#### Conclusion
Arpeggios are the weakest among the technique category, the page order and technique familiarity have relevance that the earlier the pages, the better the techniques are. 


#### Follow up
Ask my son to practice backwards, start from the Arpeggios. Also spend more time on the techinques below the average.
