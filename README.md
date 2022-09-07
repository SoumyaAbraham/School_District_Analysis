# School_District_Analysis
### Overview:
Using Python pandas library and Jupyter Notebook to analyze the performances in various schools in the district. We are looking for possible corelations in the school budgets and school size with performance. &nbsp;
There are two sets of deliverables we are looking for: &nbsp;

  1. Replacing the ninth-grade Reading and Math scores.
  2. Repeating the Student District Analysis, consisting of:
  
    a. District Summary 
    b. School Summary 
    c. Top and Bottom 5 performing schools (based on overall passing rates) 
    d. Average Math score for each grade level for each school 
    e. Average Reading score for each grade level for each school 
    f. Score by  
    
      i. School Budgets per Student per school 
      ii. School Size 
      iii. School Type 
----      

### Results:
After removing incorrect prefixes and suffixes like 'Mr., Dr., PhD' etc, our *student dataframe* looked like this:

![student_df](https://github.com/SoumyaAbraham/School_District_Analysis/blob/main/Screenshots/1.%20student_df.png)


## Deliverable 1:

In our challenge, we go a step further and replace all the scores for _Thomas High School Grade 9_ with *NaN* (Not A Number) using the .loc() function.
The resulting student dataframe looks like this:

![deliverable 1](https://github.com/SoumyaAbraham/School_District_Analysis/blob/main/Screenshots/2.%20Deliverable%201.png)

Notice that only the scores for 9th grade students from Thomas High School have been removed from the total analysis.

## Deliverable 2:

Now that we have a modified dataset to analyze, let us go through each step of the *School District Analysis* one more time.

### District Summary Dataframes:

Let us look at the *district summary dataframes* for both the original and modified analysis:  

Original:  
![district summary](https://github.com/SoumyaAbraham/School_District_Analysis/blob/main/Screenshots/3.%20district_summary.png)  

Modified:  
![new district summary](https://github.com/SoumyaAbraham/School_District_Analysis/blob/main/Screenshots/4.%20new_district_summary.png)  

Notice the subtle differences in the average and percentage scores. While it is not much, we can see the differences made by removing the grades for 9th grade Thomas High School.  


### Per School Summary Dataframes:

Next, let us look at the *per school summary dataframes* for both the original and modified analysis:  

Original:  
![per school analysis](https://github.com/SoumyaAbraham/School_District_Analysis/blob/main/Screenshots/5.%20per_school_summary.png)  

Modified:  
![new per school analysis](https://github.com/SoumyaAbraham/School_District_Analysis/blob/main/Screenshots/6.%20new_per_school_summary.png)

Let's take a look at Thomas High School. There is again a subtle drop in score percentages. Again, this is caused by the removal of their 9th grade scores.

### Top 5 Performing Schools:

When we look at the top 5 performing schools:  

Original:  
![top5](https://github.com/SoumyaAbraham/School_District_Analysis/blob/main/Screenshots/7.%20top_schools.png)  


Modified:  
![new top 5](https://github.com/SoumyaAbraham/School_District_Analysis/blob/main/Screenshots/8.%20new_top_schools.png)

Since Thomas High School is second in performance, you will notice a difference in the scores and their percentages. 

### Bottom 5 Performing Schools:  

When we look at the bottom 5 performing schools:  

Original:  
![bottom5](https://github.com/SoumyaAbraham/School_District_Analysis/blob/main/Screenshots/9.%20bottom_schools.png)  


Modified:  
![new bottom5](https://github.com/SoumyaAbraham/School_District_Analysis/blob/main/Screenshots/10.%20new_bottom_schools.png)  

Since Thomas High School is not included in this list, there is no difference in the dataframe when the analysis was redone.

### Grade Level Dataframes:  

- Average Math Score by Grades (per School)  
Let us look at the average math scores per grade  

Original:  
![av_math](https://github.com/SoumyaAbraham/School_District_Analysis/blob/main/Screenshots/11.%20av_math_perGrade.png)  


Modified:  
![new_av_math](https://github.com/SoumyaAbraham/School_District_Analysis/blob/main/Screenshots/12.%20new%20av_math_perGrade.png)

Notice that the 9th grade math average for Thomas High School is *NaN* in the new dataframe.

- Average Reading Score by Grades (per School)  
Let us look at the average reading scores per grade  

Original:  
![av_reading](https://github.com/SoumyaAbraham/School_District_Analysis/blob/main/Screenshots/13.%20av_reading_perGrade.png)  


Modified:  
![new av_reading](https://github.com/SoumyaAbraham/School_District_Analysis/blob/main/Screenshots/14.%20new%20av_reading_perGrade.png)  

Notice that the 9th grade reading average for Thomas High School is *NaN* in the new dataframe.

### Spending Summary:

Let us analyze the school performance when we take the _budget per student_ into account:  

Original:  
![spending_summary](https://github.com/SoumyaAbraham/School_District_Analysis/blob/main/Screenshots/15.%20spending_summary.png)  


Modified:  
![new_spending_summary](https://github.com/SoumyaAbraham/School_District_Analysis/blob/main/Screenshots/16.%20newspending_summary.png)

Since Thomas High School falls under the $630-$645 budget, we notice slight changes in the average scores.  
More importantly, if we take a look at the performances as the *budget per student increases*, we actually see that the *performance decreases*. From our analysis, we can infer that _a higher budget does *not* lead to better school performance_.

### Size Summary:

Now let us analyze the school performance based on the _size of the school_ :  

Original:  
![size_summary](https://github.com/SoumyaAbraham/School_District_Analysis/blob/main/Screenshots/17.%20size%20summary.png)  


Modified:  
![new size_summary](https://github.com/SoumyaAbraham/School_District_Analysis/blob/main/Screenshots/18.%20new_size%20summary.png)  

We can see that there are some minor changes between the initial and new dataframes.  
If we look at the performances as the *school size increases*, we notice there is no substantial difference in the performances in the _small_ and _medium_ bins. this could be because they are more close together in range. 
However, when they are compared to the _large_ size bin, we can see quite the drop in overall performance. From our analysis, we can infer that a _larger_ school is more susceptible to _lower performances_. 

### School type Summary:

Finally, let us analyze the school performance baed on the _type of school_ :  

Original:  
![school-type](https://github.com/SoumyaAbraham/School_District_Analysis/blob/main/Screenshots/19.%20type_summary.png)  


Modified:  
![new school type](https://github.com/SoumyaAbraham/School_District_Analysis/blob/main/Screenshots/20.%20new_type_summary.png)  

Once again, since Thomas High School is a Charter School, you will notice minute changes in the initial and new dataframes. 
However, it is very clear from the dataframes that _Charter schools_ perform _better_ than _District schools_

---

## Summary:  

*When we removed the scores for 9th grade at Thomas High School, we removed 1174 student grades out of a total 39170 student grades. That is roughly 3% of the total database. This may explain why we do not see a substantial difference in the original and modified dataframes.  

* We also noticed that the increase in budget per school showed a decrease in performance. This can be helpful when making budget plans for the new year.  
* We notice that larger schools have been performing poorer than those of a smaller size.  
* lastly, we see that Charter schools perform better than district schools.

---

You can find the original analysis here:  
[original_analysis](https://github.com/SoumyaAbraham/School_District_Analysis/blob/main/PyCitySchools.ipynb)

You can also find the modified analysis here:  
[modified_analysis](https://github.com/SoumyaAbraham/School_District_Analysis/blob/main/%20PyCitySchools_Challenge.ipynb)

---
