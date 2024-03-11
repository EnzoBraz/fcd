```python
#In: 
# Imports
import babypandas as bpd
import numpy as np

import plotly.express as px
import matplotlib.pyplot as plt
plt.style.use('ggplot')
```

# Lecture 1 – Introduction

## DSC 10, Winter 2023

### Welcome to DSC 10! 👋
- A guided tour of data science.
    - Developed by UC Berkeley in 2015.
    - Adapted by UC San Diego in 2017.
- Learn just enough programming and statistics to do data science.
    - Statistics without too much math, mostly simulation.
    - Lays the foundation for all other courses in the DSC major.

### Agenda

- Course staff.
- What is data science?
- How will this course run?
- Literature demo.

## Course staff

### Instructor: Dr. Janine Tiefenbruck (call me Janine) 👩‍🏫
- BS in Math and Computer Science at Loyola Maryland, PhD in Math (combinatorics) at UCSD 🔱.
- Teaching at UCSD: Math ➡️ CSE ➡️ DSC.
    - 9th time teaching DSC 10!
    - Also teach DSC 40A often.
- Outside interests: crafting, board games, hiking, baking 🎂.

<center>
    <table><tr>
        <td> <img src="images/cupcakes.jpg" width=300>  </td>
        <td> <img src="images/christmas2.jpg" width=300> </td>
    </tr></table>
</center>

### TAs, Tutors, and Mascot

In addition, we have several other course staff members who are here to support you in discussion, office hours, and online.

- **2 graduate TAs**: Dylan Stockard and Dasha Veraksa.
- **17 undergraduate tutors**: Gabriel Cha, Eric Chen, Charlie Gillet, Vanessa Hu, Dylan Lee, Anthony Li, Jasmine Lo, Linda Long, Aishani Mohapatra, Harshita Saha, Abel Seyoum, Selim Shaalan, Yutian (Skylar) Shi, Tony Ta, Zairan Xiang, Diego Zavalza, and Luran (Lauren) Zhang, 
- **1 stuffed panda mascot**: Baby Panda. 🐼

Learn more about them at [dsc10.com/staff](https://dsc10.com/staff).

## What is "data science"? 🤔

<center><img src='images/what-is-ds.png' width=1250>Everyone seems to have their own definition of data science.</center>

### What is "data science"?

Data science is about **drawing useful conclusions from data using computation**. Throughout the quarter, we'll touch on several aspects of data science:

- First 4 weeks: use Python to **explore** data.
    - Lots of visualization 📈📊 and "data manipulation", using industry-standard tools.

- Next 4 weeks: use data to **infer** about a population, given just a sample.
    - Rely heavily on simulation, rather than formulas.

- Last 2 weeks: use data from the past to **predict** what may happen in the future.
    - A taste of machine learning 🤖.

### Data science is more relevant than ever 🤧

We've spent the last three years looking at graphs like this:

<center><img src='images/covid.jpg' width=75%></center>

### It can be fun, too!

<center><img src='images/rapper_vocab.jpg' width=75%></center>

From [The Pudding](https://pudding.cool/)'s article on [rapper vocabularies](https://pudding.cool/projects/vocabulary/).

## Course logistics

### Course website

The course website is your one-stop-shop for all things related to the course.

<center><h3><a href="https://dsc10.com">dsc10.com</a></h3></center>

This is where lectures, homeworks, labs, discussions, and all other content will be posted. Check it often, and **read the [syllabus](https://dsc10.com/syllabus)**!

### Getting set up

- **EdStem**: Q&A forum. All announcements will be made here. You should have gotten email invitation; if not, there's a link on syllabus.
- **Gradescope**: Where you will submit all assignments for autograding, and where all of your grades will live. You should have been automatically added; contact us if not.
- **DataHub**: Where you will access and run all code in this class. Access at [datahub.ucsd.edu](https://datahub.ucsd.edu). More on Wednesday.
- We will **not** be using Canvas for anything!

In addition, you must also fill out a [Beginning of Quarter Survey](https://forms.gle/EpXSJitSUFtBiNgN9).

### Lecture

- Lectures will be in-person and recorded for viewing afterwards.
    - You can attend any of the 3 lecture sections, as long as there is space for the students officially enrolled in that section.
    - Attendance will never be required but it is incentivized through **extra credit**.
    - Recordings can be found at [podcast.ucsd.edu](https://podcast.ucsd.edu).
- Slides/code from lecture will be linked on the course website, both in a "runnable" code format and as an HTML file (✏️), which you can save as a PDF and annotate on your tablet.
- We will try to make lectures engaging. **Bring your laptop or tablet**, if you have one.

### Concept Check ✅ – Answer at [cc.dsc10.com](http://cc.dsc10.com) 

**How many of the following food items qualify as a sandwich?**

<center><img src='images/foods.png' width=30%></center>

A. 0 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 
B. 1 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
C. 2 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
D. 3 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
E. 4 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;

_(We are always going to use the same link for Concept Checks, so you should bookmark it._)



### Discussion

- Discussion sections are designed to give you practice with the **conceptual ideas** in the course.
    - All assignments in this class will be done on the computer using code, but the exams are on-paper and in-person.
    - For each discussion, we've prepared a problem set, **made up of old exam problems** (see [practice.dsc10.com](https://practice.dsc10.com)). 
    - Problem sets are posted online, so bring a computer or tablet to access them. But like exams, you will answer the problems **on paper**.
    - Discussion problem sets aren't submitted anywhere.
- Attendance is not required, however **extra credit** is provided for attending.
    - If you do attend, you must attend the discussion section you're assigned to.
    - Like lectures, discussions will be podcasted.

### Discussion Schedule

Every student is assigned to one particular discussion as follows. You can request a time change on the [Beginning of Quarter Survey](https://forms.gle/EpXSJitSUFtBiNgN9). <span style="color:red"><b>🚨 Ignore the discussion and lab time listed on your course schedule.</b></span>

<center><img src='images/discussion.jpg' width=90%></center>

### Labs

- Labs refer to **lab assignments**, which are a required part of the course and help you develop fluency in Python and working with data.
- While working on labs, you'll be able to run **autograder tests** which tell you if your answers are correct.
    - For labs, if you pass all autograder tests, you will get 100\%!
- You must submit labs individually, but you can discuss ideas with others (no sharing code).
- Labs are usually due on **Saturdays at 11:59PM** to Gradescope. The first lab (due on Saturday, January 14) will have submission instructions.

### Homeworks and projects

- Weekly homework assignments build off of skills you develop in labs.
- A key difference between homeworks and labs is that **passing autograder tests does not guarantee a perfect score!**
    - In homeworks, we have "hidden tests" that are only run after you submit the assignment.
    - The tests that are available to you within the assignment itself only verify that your answer is reasonable/on the right track.
- Again, you must work on homeworks yourself, but you can discuss ideas with other students (no sharing code).
- Homeworks are usually due on **Tuesdays at 11:59PM** and submitted to Gradescope.
- In the **Midterm Project** and **Final Project**, you will do a deep dive into a dataset! Projects are longer than homeworks, so we give you more time to work on them.
    - This quarter's projects: Restaurants 🍔 and Great British Bake Off Great British Bake Off 👩‍🍳🍰.
    - You can work on projects with partners, following these [project partner guidelines](https://dsc10.com/project-partners). Both of you should actively contribute to **all parts** of the project.

### Exams

We will have two exams this quarter.
- **Midterm Exam**: Friday, February 10th, during your scheduled lecture time.
- **Final Exam**: Saturday, March 18th, 3-6pm.
- Both exams will be conducted in person and on paper. Let us know if you have a conflict in the [Beginning of Quarter Survey](https://forms.gle/EpXSJitSUFtBiNgN9).

### Readings and resources

- We will draw readings from two sources. Readings for each lecture will be posted on the course homepage.
    - [Computational and Inferential Thinking (CIT)](https://inferentialthinking.com), the textbook created for Berkeley's version of this course.
    - [`babypandas` notes](https://notes.dsc10.com), written specifically for the first part of DSC 10.
- The [Resources](https://dsc10.com/resources) tab of the course website contains links to helpful resources that you'll want to use throughout the course (e.g. DSC 10 Reference Sheet, programming tutorials, supplemental videos).
- The [Debugging](https://dsc10.com/debugging) tab of the course website has answers to many common technical issues.

### A typical week in DSC 10

| Sunday | Monday | Tuesday | Wednesday | Thursday | Friday | Saturday |
|: -- :|: -- :|: -- :|: -- :|: -- :|: -- :|: -- :|
| Nothing! 😎 | Lecture | | Lecture | | Lecture | |
| | | | Discussion | | | |
| | | **HW due** | | | | **Lab due** |

See the [Syllabus](https://dsc10.com/syllabus) for more details.

### First assignment
- Lab 0 is due **Saturday, January 14th at 11:59PM**.
    - Will be released later today
- <span style='color:red'><b>🚨 Important: Start early and submit often</b>.</span>

### Getting help
This is a tough, fast-paced course, but we're here to help you – here's how:

- **Office Hours (OH)**.
    - Remote and in-person throughout the week.
    - See the schedule and Zoom link on the [Calendar 📆](https://dsc10.com/calendar).
- **EdStem**.
    - Post here with any logistical or conceptual questions (please don't email).
    - No code or solutions in public posts. Such posts should be private to instructors + staff.
    - Otherwise, post publicly (anonymously, if you'd like).
- <span style="color:red;"><b>🚨 Important: Use these to your advantage!</b></span>

### Opportunity: Python bootcamp

Diversity in Data Science, a student organization, is running a one-week Python bootcamp specifically **for students in DSC 10 with no prior programming experience**. The bootcamp is **this week**. Sign up [here](https://docs.google.com/forms/d/e/1FAIpQLSdlRXdN6hzlC8IWGA8iuABDseRFkX22m2nATTQRJvkg_DTyPg/viewform).


<center><img src='images/bootcamp.png' width=40%></center>

### Advice from previous students

At the end of each quarter, we ask DSC 10 students to give advice to future students in the course. Here are some responses:

> "Go to office hours! Get a partner for the project even if you don't want to. If you don't understand a topic try the following: go to office hours, ask on [EdStem], check the [readings], look at lecture notes. Start on the assignments early try and finish 2 days early to check your work."

> "I would give the advice to attend the discussions and office hours whenever possible, as a lot of the times I found myself learning new things even when I didn't come with a question ready."

> "Do NOT fall behind in lectures. It becomes very difficult to catch up on the concepts. Go to your discussion section! Hearing a concept explained once can be difficult to understand so discussion section was extremely helpful."

> "GO TO OFFICE HOURS!  It's very important to let your voice out. Talk to the professor after lectures, attend office hours, post your questions and ask a question."

### Collaboration

#### Asking questions is highly encouraged!
- Discuss all questions with each other (except exams).
- Submit lab assignments individually, but you can work with others (no sharing code).
- Submit homeworks individually, but you can discuss problem-solving strategies with others (no sharing code).
- Submit projects individually or in pairs using pair programming.

#### The limits of collaboration:
- Don't share solutions with each other or look at someone’s code.
- Project partners should both contribute to all parts of the project. Don't split up the project.
- Academic integrity violations usually result in failing the course. 

### We're here for you!

Regardless of your background, you can succeed in this course. **No prior programming or statistics experience will be assumed!**

Watch on YouTube: [We’re All Data Scientists | Rebecca Nugent | TEDxCMU](https://www.youtube.com/watch?v=YMnqPTLoj7o).

### Campus resources

Counseling and Psychological Services (CAPS) is a campus unit that offers “short term counseling for academic, career, and personal issues and also offers psychiatry services for circumstances when medication can help with counseling.”
If you or anyone you know is ever in need of mental health care, you should contact CAPS.

<center><h3><a href="https://caps.ucsd.edu/">caps.ucsd.edu</a></h3></center>

## Demo

### _Little Women_ (1868)

- _Little Women_, by Louisa May Alcott, is a novel that follows the life of four sisters – Meg, Jo, Beth, and Amy.
- Using tools from this class, we'll learn (a bit) about the plot of the book, without reading it.
- Do not worry about any of this code – we'll cover the necessary pieces in the weeks to come. Sit back and relax!


```python
#In: 
# Read in 'lw.txt' to a variable called "little_women_text"
little_women_text = open('data/lw.txt').read()
```


```python
#In: 
# See the first three thousand characters
little_women_text[:3000]
```




    'The Project Gutenberg EBook of Little Women, by Louisa May Alcott\n\nThis eBook is for the use of anyone anywhere at no cost and with\nalmost no restrictions whatsoever.  You may copy it, give it away or\nre-use it under the terms of the Project Gutenberg License included\nwith this eBook or online at www.gutenberg.net\n\n\nTitle: Little Women\n\nAuthor: Louisa May Alcott\n\nPosting Date: September 13, 2008 [EBook #514]\nRelease Date: May, 1996\n[This file last updated on August 19, 2010]\n\nLanguage: English\n\n\n*** START OF THIS PROJECT GUTENBERG EBOOK LITTLE WOMEN ***\n\n\n\n\nLITTLE WOMEN\n\n\nby\n\nLouisa May Alcott\n\n\n\n\nCONTENTS\n\n\nPART 1\n\n          ONE  PLAYING PILGRIMS\n          TWO  A MERRY CHRISTMAS\n        THREE  THE LAURENCE BOY\n         FOUR  BURDENS\n         FIVE  BEING NEIGHBORLY\n          SIX  BETH FINDS THE PALACE BEAUTIFUL\n        SEVEN  AMY\'S VALLEY OF HUMILIATION\n        EIGHT  JO MEETS APOLLYON\n         NINE  MEG GOES TO VANITY FAIR\n          TEN  THE P.C. AND P.O.\n       ELEVEN  EXPERIMENTS\n       TWELVE  CAMP LAURENCE\n     THIRTEEN  CASTLES IN THE AIR\n     FOURTEEN  SECRETS\n      FIFTEEN  A TELEGRAM\n      SIXTEEN  LETTERS\n    SEVENTEEN  LITTLE FAITHFUL\n     EIGHTEEN  DARK DAYS\n     NINETEEN  AMY\'S WILL\n       TWENTY  CONFIDENTIAL\n   TWENTY-ONE  LAURIE MAKES MISCHIEF, AND JO MAKES PEACE\n   TWENTY-TWO  PLEASANT MEADOWS\n TWENTY-THREE  AUNT MARCH SETTLES THE QUESTION\n\n\nPART 2\n\n  TWENTY-FOUR  GOSSIP\n  TWENTY-FIVE  THE FIRST WEDDING\n   TWENTY-SIX  ARTISTIC ATTEMPTS\n TWENTY-SEVEN  LITERARY LESSONS\n TWENTY-EIGHT  DOMESTIC EXPERIENCES\n  TWENTY-NINE  CALLS\n       THIRTY  CONSEQUENCES\n   THIRTY-ONE  OUR FOREIGN CORRESPONDENT\n   THIRTY-TWO  TENDER TROUBLES\n THIRTY-THREE  JO\'S JOURNAL\n  THIRTY-FOUR  FRIEND\n  THIRTY-FIVE  HEARTACHE\n   THIRTY-SIX  BETH\'S SECRET\n THIRTY-SEVEN  NEW IMPRESSIONS\n THIRTY-EIGHT  ON THE SHELF\n  THIRTY-NINE  LAZY LAURENCE\n        FORTY  THE VALLEY OF THE SHADOW\n    FORTY-ONE  LEARNING TO FORGET\n    FORTY-TWO  ALL ALONE\n  FORTY-THREE  SURPRISES\n   FORTY-FOUR  MY LORD AND LADY\n   FORTY-FIVE  DAISY AND DEMI\n    FORTY-SIX  UNDER THE UMBRELLA\n  FORTY-SEVEN  HARVEST TIME\n\n\n\nCHAPTER ONE\n\nPLAYING PILGRIMS\n\n"Christmas won\'t be Christmas without any presents," grumbled Jo, lying\non the rug.\n\n"It\'s so dreadful to be poor!" sighed Meg, looking down at her old\ndress.\n\n"I don\'t think it\'s fair for some girls to have plenty of pretty\nthings, and other girls nothing at all," added little Amy, with an\ninjured sniff.\n\n"We\'ve got Father and Mother, and each other," said Beth contentedly\nfrom her corner.\n\nThe four young faces on which the firelight shone brightened at the\ncheerful words, but darkened again as Jo said sadly, "We haven\'t got\nFather, and shall not have him for a long time." She didn\'t say\n"perhaps never," but each silently added it, thinking of Father far\naway, where the fighting was.\n\nNobody spoke for a minute; then Meg said in an altered tone, "You know\nthe reason Mother proposed not having any presents this Christmas was\nbecause it is going to b'




```python
#In: 
# Print the first three thousand characters
print(little_women_text[:3000])
```

    The Project Gutenberg EBook of Little Women, by Louisa May Alcott
    
    This eBook is for the use of anyone anywhere at no cost and with
    almost no restrictions whatsoever.  You may copy it, give it away or
    re-use it under the terms of the Project Gutenberg License included
    with this eBook or online at www.gutenberg.net
    
    
    Title: Little Women
    
    Author: Louisa May Alcott
    
    Posting Date: September 13, 2008 [EBook #514]
    Release Date: May, 1996
    [This file last updated on August 19, 2010]
    
    Language: English
    
    
    *** START OF THIS PROJECT GUTENBERG EBOOK LITTLE WOMEN ***
    
    
    
    
    LITTLE WOMEN
    
    
    by
    
    Louisa May Alcott
    
    
    
    
    CONTENTS
    
    
    PART 1
    
              ONE  PLAYING PILGRIMS
              TWO  A MERRY CHRISTMAS
            THREE  THE LAURENCE BOY
             FOUR  BURDENS
             FIVE  BEING NEIGHBORLY
              SIX  BETH FINDS THE PALACE BEAUTIFUL
            SEVEN  AMY'S VALLEY OF HUMILIATION
            EIGHT  JO MEETS APOLLYON
             NINE  MEG GOES TO VANITY FAIR
              TEN  THE P.C. AND P.O.
           ELEVEN  EXPERIMENTS
           TWELVE  CAMP LAURENCE
         THIRTEEN  CASTLES IN THE AIR
         FOURTEEN  SECRETS
          FIFTEEN  A TELEGRAM
          SIXTEEN  LETTERS
        SEVENTEEN  LITTLE FAITHFUL
         EIGHTEEN  DARK DAYS
         NINETEEN  AMY'S WILL
           TWENTY  CONFIDENTIAL
       TWENTY-ONE  LAURIE MAKES MISCHIEF, AND JO MAKES PEACE
       TWENTY-TWO  PLEASANT MEADOWS
     TWENTY-THREE  AUNT MARCH SETTLES THE QUESTION
    
    
    PART 2
    
      TWENTY-FOUR  GOSSIP
      TWENTY-FIVE  THE FIRST WEDDING
       TWENTY-SIX  ARTISTIC ATTEMPTS
     TWENTY-SEVEN  LITERARY LESSONS
     TWENTY-EIGHT  DOMESTIC EXPERIENCES
      TWENTY-NINE  CALLS
           THIRTY  CONSEQUENCES
       THIRTY-ONE  OUR FOREIGN CORRESPONDENT
       THIRTY-TWO  TENDER TROUBLES
     THIRTY-THREE  JO'S JOURNAL
      THIRTY-FOUR  FRIEND
      THIRTY-FIVE  HEARTACHE
       THIRTY-SIX  BETH'S SECRET
     THIRTY-SEVEN  NEW IMPRESSIONS
     THIRTY-EIGHT  ON THE SHELF
      THIRTY-NINE  LAZY LAURENCE
            FORTY  THE VALLEY OF THE SHADOW
        FORTY-ONE  LEARNING TO FORGET
        FORTY-TWO  ALL ALONE
      FORTY-THREE  SURPRISES
       FORTY-FOUR  MY LORD AND LADY
       FORTY-FIVE  DAISY AND DEMI
        FORTY-SIX  UNDER THE UMBRELLA
      FORTY-SEVEN  HARVEST TIME
    
    
    
    CHAPTER ONE
    
    PLAYING PILGRIMS
    
    "Christmas won't be Christmas without any presents," grumbled Jo, lying
    on the rug.
    
    "It's so dreadful to be poor!" sighed Meg, looking down at her old
    dress.
    
    "I don't think it's fair for some girls to have plenty of pretty
    things, and other girls nothing at all," added little Amy, with an
    injured sniff.
    
    "We've got Father and Mother, and each other," said Beth contentedly
    from her corner.
    
    The four young faces on which the firelight shone brightened at the
    cheerful words, but darkened again as Jo said sadly, "We haven't got
    Father, and shall not have him for a long time." She didn't say
    "perhaps never," but each silently added it, thinking of Father far
    away, where the fighting was.
    
    Nobody spoke for a minute; then Meg said in an altered tone, "You know
    the reason Mother proposed not having any presents this Christmas was
    because it is going to b



```python
#In: 
# Create a variable "chapters" by splitting the text on 'CHAPTER '
chapters = little_women_text.split('CHAPTER ') 

# Create a DataFrame with one column -- the chapters
bpd.DataFrame().assign(chapters=chapters)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>chapters</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>The Project Gutenberg EBook of Little Women, b...</td>
    </tr>
    <tr>
      <th>1</th>
      <td>ONE\n\nPLAYING PILGRIMS\n\n"Christmas won't be...</td>
    </tr>
    <tr>
      <th>2</th>
      <td>TWO\n\nA MERRY CHRISTMAS\n\nJo was the first t...</td>
    </tr>
    <tr>
      <th>3</th>
      <td>THREE\n\nTHE LAURENCE BOY\n\n"Jo!  Jo!  Where ...</td>
    </tr>
    <tr>
      <th>4</th>
      <td>FOUR\n\nBURDENS\n\n"Oh, dear, how hard it does...</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
    </tr>
    <tr>
      <th>43</th>
      <td>FORTY-THREE\n\nSURPRISES\n\nJo was alone in th...</td>
    </tr>
    <tr>
      <th>44</th>
      <td>FORTY-FOUR\n\nMY LORD AND LADY\n\n"Please, Mad...</td>
    </tr>
    <tr>
      <th>45</th>
      <td>FORTY-FIVE\n\nDAISY AND DEMI\n\nI cannot feel ...</td>
    </tr>
    <tr>
      <th>46</th>
      <td>FORTY-SIX\n\nUNDER THE UMBRELLA\n\nWhile Lauri...</td>
    </tr>
    <tr>
      <th>47</th>
      <td>FORTY-SEVEN\n\nHARVEST TIME\n\nFor a year Jo a...</td>
    </tr>
  </tbody>
</table>
<p>48 rows × 1 columns</p>
</div>




```python
#In: 
# Counts of names in the chapters of Little Women

counts = bpd.DataFrame().assign(
    Amy=np.char.count(chapters, 'Amy'),
    Beth=np.char.count(chapters, 'Beth'),
    Jo=np.char.count(chapters, 'Jo'),
    Meg=np.char.count(chapters, 'Meg'),
    Laurie=np.char.count(chapters, 'Laurie'),
)
counts
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Amy</th>
      <th>Beth</th>
      <th>Jo</th>
      <th>Meg</th>
      <th>Laurie</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>23</td>
      <td>26</td>
      <td>44</td>
      <td>26</td>
      <td>0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>13</td>
      <td>12</td>
      <td>21</td>
      <td>20</td>
      <td>0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2</td>
      <td>2</td>
      <td>62</td>
      <td>36</td>
      <td>16</td>
    </tr>
    <tr>
      <th>4</th>
      <td>14</td>
      <td>18</td>
      <td>34</td>
      <td>17</td>
      <td>0</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>43</th>
      <td>31</td>
      <td>8</td>
      <td>61</td>
      <td>3</td>
      <td>29</td>
    </tr>
    <tr>
      <th>44</th>
      <td>13</td>
      <td>0</td>
      <td>9</td>
      <td>0</td>
      <td>10</td>
    </tr>
    <tr>
      <th>45</th>
      <td>1</td>
      <td>2</td>
      <td>6</td>
      <td>2</td>
      <td>0</td>
    </tr>
    <tr>
      <th>46</th>
      <td>2</td>
      <td>1</td>
      <td>56</td>
      <td>4</td>
      <td>2</td>
    </tr>
    <tr>
      <th>47</th>
      <td>10</td>
      <td>3</td>
      <td>37</td>
      <td>6</td>
      <td>13</td>
    </tr>
  </tbody>
</table>
<p>48 rows × 5 columns</p>
</div>




```python
#In: 
# Cumulative number of times each name appears

cumulative_counts = bpd.DataFrame().assign(
    Amy=np.cumsum(counts.get('Amy')),
    Beth=np.cumsum(counts.get('Beth')),
    Jo=np.cumsum(counts.get('Jo')),
    Meg=np.cumsum(counts.get('Meg')),
    Laurie=np.cumsum(counts.get('Laurie')),
    Chapter=np.arange(1, 49, 1)
)

cumulative_counts.plot(x='Chapter', figsize=(10, 5))

plt.title('Cumulative Number of Times Each Name Appears', y=1.08);
```


    
![png](lec01_files/lec01_43_0.png)
    



```python
#In: 
# Interactive version of the previous plot

cumulative_counts_df = cumulative_counts.drop(columns=['Chapter']).to_df().melt().rename(columns={'variable': 'name', 'value': 'count'})
cumulative_counts_df = cumulative_counts_df.assign(chapter = list(range(1, 49)) * 5)
px.line(cumulative_counts_df, x='chapter', y='count', color='name', width=900, height=600, title='Cumulative Number of Times Each Name Appears')
```


        <script type="text/javascript">
        window.PlotlyConfig = {MathJaxConfig: 'local'};
        if (window.MathJax && window.MathJax.Hub && window.MathJax.Hub.Config) {window.MathJax.Hub.Config({SVG: {font: "STIX-Web"}});}
        if (typeof require !== 'undefined') {
        require.undef("plotly");
        define('plotly', function(require, exports, module) {
            /**
* plotly.js v2.29.1
* Copyright 2012-2024, Plotly, Inc.
* All rights reserved.
* Licensed under the MIT license
*/
/*! For license information please see plotly.min.js.LICENSE.txt */
        });
        require(['plotly'], function(Plotly) {
            window._Plotly = Plotly;
        });
        }
        </script>




<div>                            <div id="c8ad7042-2384-42d2-b626-21c97f807749" class="plotly-graph-div" style="height:600px; width:900px;"></div>            <script type="text/javascript">                require(["plotly"], function(Plotly) {                    window.PLOTLYENV=window.PLOTLYENV || {};                                    if (document.getElementById("c8ad7042-2384-42d2-b626-21c97f807749")) {                    Plotly.newPlot(                        "c8ad7042-2384-42d2-b626-21c97f807749",                        [{"hovertemplate":"name=Amy\u003cbr\u003echapter=%{x}\u003cbr\u003ecount=%{y}\u003cextra\u003e\u003c\u002fextra\u003e","legendgroup":"Amy","line":{"color":"#636efa","dash":"solid"},"marker":{"symbol":"circle"},"mode":"lines","name":"Amy","orientation":"v","showlegend":true,"x":[1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,31,32,33,34,35,36,37,38,39,40,41,42,43,44,45,46,47,48],"xaxis":"x","y":[0,23,36,38,52,58,64,91,139,142,147,164,175,183,189,197,204,223,226,256,265,267,276,283,298,305,342,345,348,394,451,456,463,468,468,468,471,502,502,547,548,581,588,619,632,633,635,645],"yaxis":"y","type":"scatter"},{"hovertemplate":"name=Beth\u003cbr\u003echapter=%{x}\u003cbr\u003ecount=%{y}\u003cextra\u003e\u003c\u002fextra\u003e","legendgroup":"Beth","line":{"color":"#EF553B","dash":"solid"},"marker":{"symbol":"circle"},"mode":"lines","name":"Beth","orientation":"v","showlegend":true,"x":[1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,31,32,33,34,35,36,37,38,39,40,41,42,43,44,45,46,47,48],"xaxis":"x","y":[0,26,38,40,58,72,100,105,114,119,124,144,164,177,182,194,203,232,262,269,276,277,292,298,307,313,318,322,322,323,328,331,364,370,372,375,412,413,413,414,435,442,451,459,459,461,462,465],"yaxis":"y","type":"scatter"},{"hovertemplate":"name=Jo\u003cbr\u003echapter=%{x}\u003cbr\u003ecount=%{y}\u003cextra\u003e\u003c\u002fextra\u003e","legendgroup":"Jo","line":{"color":"#00cc96","dash":"solid"},"marker":{"symbol":"circle"},"mode":"lines","name":"Jo","orientation":"v","showlegend":true,"x":[1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,31,32,33,34,35,36,37,38,39,40,41,42,43,44,45,46,47,48],"xaxis":"x","y":[0,44,65,127,161,216,229,238,309,330,342,384,444,468,516,542,555,584,619,624,653,720,737,788,824,836,853,881,950,999,1038,1045,1105,1107,1162,1204,1239,1244,1291,1306,1321,1338,1374,1435,1444,1450,1506,1543],"yaxis":"y","type":"scatter"},{"hovertemplate":"name=Meg\u003cbr\u003echapter=%{x}\u003cbr\u003ecount=%{y}\u003cextra\u003e\u003c\u002fextra\u003e","legendgroup":"Meg","line":{"color":"#ab63fa","dash":"solid"},"marker":{"symbol":"circle"},"mode":"lines","name":"Meg","orientation":"v","showlegend":true,"x":[1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,31,32,33,34,35,36,37,38,39,40,41,42,43,44,45,46,47,48],"xaxis":"x","y":[0,26,46,82,99,112,117,122,138,209,213,237,278,299,320,338,353,374,388,389,414,445,454,510,539,554,559,561,613,615,615,616,619,620,620,622,625,625,665,666,667,667,670,673,673,675,679,685],"yaxis":"y","type":"scatter"},{"hovertemplate":"name=Laurie\u003cbr\u003echapter=%{x}\u003cbr\u003ecount=%{y}\u003cextra\u003e\u003c\u002fextra\u003e","legendgroup":"Laurie","line":{"color":"#FFA15A","dash":"solid"},"marker":{"symbol":"circle"},"mode":"lines","name":"Laurie","orientation":"v","showlegend":true,"x":[1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,31,32,33,34,35,36,37,38,39,40,41,42,43,44,45,46,47,48],"xaxis":"x","y":[0,0,0,16,16,51,60,67,84,108,112,123,154,181,202,210,219,231,253,269,274,300,308,319,339,350,355,355,366,369,381,384,405,406,408,442,445,471,471,504,504,538,542,571,581,581,583,596],"yaxis":"y","type":"scatter"}],                        {"template":{"data":{"histogram2dcontour":[{"type":"histogram2dcontour","colorbar":{"outlinewidth":0,"ticks":""},"colorscale":[[0.0,"#0d0887"],[0.1111111111111111,"#46039f"],[0.2222222222222222,"#7201a8"],[0.3333333333333333,"#9c179e"],[0.4444444444444444,"#bd3786"],[0.5555555555555556,"#d8576b"],[0.6666666666666666,"#ed7953"],[0.7777777777777778,"#fb9f3a"],[0.8888888888888888,"#fdca26"],[1.0,"#f0f921"]]}],"choropleth":[{"type":"choropleth","colorbar":{"outlinewidth":0,"ticks":""}}],"histogram2d":[{"type":"histogram2d","colorbar":{"outlinewidth":0,"ticks":""},"colorscale":[[0.0,"#0d0887"],[0.1111111111111111,"#46039f"],[0.2222222222222222,"#7201a8"],[0.3333333333333333,"#9c179e"],[0.4444444444444444,"#bd3786"],[0.5555555555555556,"#d8576b"],[0.6666666666666666,"#ed7953"],[0.7777777777777778,"#fb9f3a"],[0.8888888888888888,"#fdca26"],[1.0,"#f0f921"]]}],"heatmap":[{"type":"heatmap","colorbar":{"outlinewidth":0,"ticks":""},"colorscale":[[0.0,"#0d0887"],[0.1111111111111111,"#46039f"],[0.2222222222222222,"#7201a8"],[0.3333333333333333,"#9c179e"],[0.4444444444444444,"#bd3786"],[0.5555555555555556,"#d8576b"],[0.6666666666666666,"#ed7953"],[0.7777777777777778,"#fb9f3a"],[0.8888888888888888,"#fdca26"],[1.0,"#f0f921"]]}],"heatmapgl":[{"type":"heatmapgl","colorbar":{"outlinewidth":0,"ticks":""},"colorscale":[[0.0,"#0d0887"],[0.1111111111111111,"#46039f"],[0.2222222222222222,"#7201a8"],[0.3333333333333333,"#9c179e"],[0.4444444444444444,"#bd3786"],[0.5555555555555556,"#d8576b"],[0.6666666666666666,"#ed7953"],[0.7777777777777778,"#fb9f3a"],[0.8888888888888888,"#fdca26"],[1.0,"#f0f921"]]}],"contourcarpet":[{"type":"contourcarpet","colorbar":{"outlinewidth":0,"ticks":""}}],"contour":[{"type":"contour","colorbar":{"outlinewidth":0,"ticks":""},"colorscale":[[0.0,"#0d0887"],[0.1111111111111111,"#46039f"],[0.2222222222222222,"#7201a8"],[0.3333333333333333,"#9c179e"],[0.4444444444444444,"#bd3786"],[0.5555555555555556,"#d8576b"],[0.6666666666666666,"#ed7953"],[0.7777777777777778,"#fb9f3a"],[0.8888888888888888,"#fdca26"],[1.0,"#f0f921"]]}],"surface":[{"type":"surface","colorbar":{"outlinewidth":0,"ticks":""},"colorscale":[[0.0,"#0d0887"],[0.1111111111111111,"#46039f"],[0.2222222222222222,"#7201a8"],[0.3333333333333333,"#9c179e"],[0.4444444444444444,"#bd3786"],[0.5555555555555556,"#d8576b"],[0.6666666666666666,"#ed7953"],[0.7777777777777778,"#fb9f3a"],[0.8888888888888888,"#fdca26"],[1.0,"#f0f921"]]}],"mesh3d":[{"type":"mesh3d","colorbar":{"outlinewidth":0,"ticks":""}}],"scatter":[{"fillpattern":{"fillmode":"overlay","size":10,"solidity":0.2},"type":"scatter"}],"parcoords":[{"type":"parcoords","line":{"colorbar":{"outlinewidth":0,"ticks":""}}}],"scatterpolargl":[{"type":"scatterpolargl","marker":{"colorbar":{"outlinewidth":0,"ticks":""}}}],"bar":[{"error_x":{"color":"#2a3f5f"},"error_y":{"color":"#2a3f5f"},"marker":{"line":{"color":"#E5ECF6","width":0.5},"pattern":{"fillmode":"overlay","size":10,"solidity":0.2}},"type":"bar"}],"scattergeo":[{"type":"scattergeo","marker":{"colorbar":{"outlinewidth":0,"ticks":""}}}],"scatterpolar":[{"type":"scatterpolar","marker":{"colorbar":{"outlinewidth":0,"ticks":""}}}],"histogram":[{"marker":{"pattern":{"fillmode":"overlay","size":10,"solidity":0.2}},"type":"histogram"}],"scattergl":[{"type":"scattergl","marker":{"colorbar":{"outlinewidth":0,"ticks":""}}}],"scatter3d":[{"type":"scatter3d","line":{"colorbar":{"outlinewidth":0,"ticks":""}},"marker":{"colorbar":{"outlinewidth":0,"ticks":""}}}],"scattermapbox":[{"type":"scattermapbox","marker":{"colorbar":{"outlinewidth":0,"ticks":""}}}],"scatterternary":[{"type":"scatterternary","marker":{"colorbar":{"outlinewidth":0,"ticks":""}}}],"scattercarpet":[{"type":"scattercarpet","marker":{"colorbar":{"outlinewidth":0,"ticks":""}}}],"carpet":[{"aaxis":{"endlinecolor":"#2a3f5f","gridcolor":"white","linecolor":"white","minorgridcolor":"white","startlinecolor":"#2a3f5f"},"baxis":{"endlinecolor":"#2a3f5f","gridcolor":"white","linecolor":"white","minorgridcolor":"white","startlinecolor":"#2a3f5f"},"type":"carpet"}],"table":[{"cells":{"fill":{"color":"#EBF0F8"},"line":{"color":"white"}},"header":{"fill":{"color":"#C8D4E3"},"line":{"color":"white"}},"type":"table"}],"barpolar":[{"marker":{"line":{"color":"#E5ECF6","width":0.5},"pattern":{"fillmode":"overlay","size":10,"solidity":0.2}},"type":"barpolar"}],"pie":[{"automargin":true,"type":"pie"}]},"layout":{"autotypenumbers":"strict","colorway":["#636efa","#EF553B","#00cc96","#ab63fa","#FFA15A","#19d3f3","#FF6692","#B6E880","#FF97FF","#FECB52"],"font":{"color":"#2a3f5f"},"hovermode":"closest","hoverlabel":{"align":"left"},"paper_bgcolor":"white","plot_bgcolor":"#E5ECF6","polar":{"bgcolor":"#E5ECF6","angularaxis":{"gridcolor":"white","linecolor":"white","ticks":""},"radialaxis":{"gridcolor":"white","linecolor":"white","ticks":""}},"ternary":{"bgcolor":"#E5ECF6","aaxis":{"gridcolor":"white","linecolor":"white","ticks":""},"baxis":{"gridcolor":"white","linecolor":"white","ticks":""},"caxis":{"gridcolor":"white","linecolor":"white","ticks":""}},"coloraxis":{"colorbar":{"outlinewidth":0,"ticks":""}},"colorscale":{"sequential":[[0.0,"#0d0887"],[0.1111111111111111,"#46039f"],[0.2222222222222222,"#7201a8"],[0.3333333333333333,"#9c179e"],[0.4444444444444444,"#bd3786"],[0.5555555555555556,"#d8576b"],[0.6666666666666666,"#ed7953"],[0.7777777777777778,"#fb9f3a"],[0.8888888888888888,"#fdca26"],[1.0,"#f0f921"]],"sequentialminus":[[0.0,"#0d0887"],[0.1111111111111111,"#46039f"],[0.2222222222222222,"#7201a8"],[0.3333333333333333,"#9c179e"],[0.4444444444444444,"#bd3786"],[0.5555555555555556,"#d8576b"],[0.6666666666666666,"#ed7953"],[0.7777777777777778,"#fb9f3a"],[0.8888888888888888,"#fdca26"],[1.0,"#f0f921"]],"diverging":[[0,"#8e0152"],[0.1,"#c51b7d"],[0.2,"#de77ae"],[0.3,"#f1b6da"],[0.4,"#fde0ef"],[0.5,"#f7f7f7"],[0.6,"#e6f5d0"],[0.7,"#b8e186"],[0.8,"#7fbc41"],[0.9,"#4d9221"],[1,"#276419"]]},"xaxis":{"gridcolor":"white","linecolor":"white","ticks":"","title":{"standoff":15},"zerolinecolor":"white","automargin":true,"zerolinewidth":2},"yaxis":{"gridcolor":"white","linecolor":"white","ticks":"","title":{"standoff":15},"zerolinecolor":"white","automargin":true,"zerolinewidth":2},"scene":{"xaxis":{"backgroundcolor":"#E5ECF6","gridcolor":"white","linecolor":"white","showbackground":true,"ticks":"","zerolinecolor":"white","gridwidth":2},"yaxis":{"backgroundcolor":"#E5ECF6","gridcolor":"white","linecolor":"white","showbackground":true,"ticks":"","zerolinecolor":"white","gridwidth":2},"zaxis":{"backgroundcolor":"#E5ECF6","gridcolor":"white","linecolor":"white","showbackground":true,"ticks":"","zerolinecolor":"white","gridwidth":2}},"shapedefaults":{"line":{"color":"#2a3f5f"}},"annotationdefaults":{"arrowcolor":"#2a3f5f","arrowhead":0,"arrowwidth":1},"geo":{"bgcolor":"white","landcolor":"#E5ECF6","subunitcolor":"white","showland":true,"showlakes":true,"lakecolor":"white"},"title":{"x":0.05},"mapbox":{"style":"light"}}},"xaxis":{"anchor":"y","domain":[0.0,1.0],"title":{"text":"chapter"}},"yaxis":{"anchor":"x","domain":[0.0,1.0],"title":{"text":"count"}},"legend":{"title":{"text":"name"},"tracegroupgap":0},"title":{"text":"Cumulative Number of Times Each Name Appears"},"height":600,"width":900},                        {"responsive": true}                    ).then(function(){

var gd = document.getElementById('c8ad7042-2384-42d2-b626-21c97f807749');
var x = new MutationObserver(function (mutations, observer) {{
        var display = window.getComputedStyle(gd).display;
        if (!display || display === 'none') {{
            console.log([gd, 'removed!']);
            Plotly.purge(gd);
            observer.disconnect();
        }}
}});

// Listen for the removal of the full notebook cells
var notebookContainer = gd.closest('#notebook-container');
if (notebookContainer) {{
    x.observe(notebookContainer, {childList: true});
}}

// Listen for the clearing of the current output cell
var outputEl = gd.closest('.output');
if (outputEl) {{
    x.observe(outputEl, {childList: true});
}}

                        })                };                });            </script>        </div>


### Concept Check ✅ – Answer at [cc.dsc10.com](http://cc.dsc10.com) 

In Chapter 32, Jo moves to New York alone. Her relationship with which sister suffers the most from this faraway move?

A. Amy

B. Beth

C. Meg

### Concept Check ✅ – Answer at [cc.dsc10.com](http://cc.dsc10.com) 

Laurie is a man who marries one of the sisters at the end. Which one?


A. Amy

B. Beth

C. Jo

D. Meg

### Next time

- On Wednesday, we'll start programming 💻 in Python 🐍. 
- Stay tuned for an announcement through EdStem about whether Wednesday's class will be remote or in-person. Either way, in-person discussion sections will start on Wednesday!