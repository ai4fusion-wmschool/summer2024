---
theme: default
#background: https://source.unsplash.com/1600x900/?nature,water
background: https://source.unsplash.com/collection/94734566/1920x1080
class: text-center
highlighter: shiki
lineNumbers: false
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
drawings:
  persist: false
transition: slide-left
title: Welcome to DATA 201
mdc: true
---


# Welcome to DATA 201

Intro to Data Science

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    Press Space for next page <carbon:arrow-right class="inline"/>
  </span>
</div>

<div class="abs-br m-6 flex gap-2">
  <button @click="$slidev.nav.openInEditor()" title="Open in Editor" class="text-xl slidev-icon-btn opacity-50 !border-none !hover:text-white">
    <carbon:edit />
  </button>
  <a href="https://github.com/dvasiliu/Intro-to-Data-Science" target="_blank" alt="GitHub" title="Open in GitHub"
    class="text-xl slidev-icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-logo-github />
  </a>
</div>

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---
transition: fade-out
preload: false
clicks: 4
---
# What is Data Science?


A good way to answer this question is to think of older, and well established "relatives."

<v-clicks>

- 📈 **Statistics** - A mathematical discipline concerned with the collection, description, and interpretation of data.

- 🖥️ **Computer Science** - The study of algorithms, data structures and programming methodologies.

- ⓘ **Information Science** - A field primarily concerned with the analysis, collection, classification, manipulation, storage, retrieval, movement, dissemination, and protection of information. 


</v-clicks>

<p v-if="$slidev.nav.clicks === 4">

<div class="w-60 relative mt-6">
  <div class="relative w-40 h-40">
    <img
      v-motion
      :initial="{ x: 800, y: -100, scale: 1.5, rotate: -50 }"
      :enter="final"
      class="absolute top-0 left-20 right-0 bottom-0"
      src="https://sli.dev/logo-circle.png"
      alt=""
    />
        <img
      v-motion
      :initial="{ x: -200, y: -100, scale: 1.5, rotate: -50 }"
      :enter="final"
      class="absolute top-0 left-0 right-0 bottom-0"
      src="https://sli.dev/logo-circle.png"
      alt=""
    />
    <img
      v-motion
      :initial="{ y: 500, x: -100, scale: 4 }"
      :enter="finalb"
      class="absolute top-20 left-0 right-20 bottom-0"
      src="https://sli.dev/logo-circle.png"
      alt=""
    />
    <img
      v-motion
      :initial="{ x: 600, y: 400, scale: 2, rotate: 100 }"
      :enter="finals"
      class="absolute top-0 left-0 right-0 bottom-0"
      src="https://sli.dev/logo-triangle.png"
      alt=""
    />
  </div>
</div>



<!-- vue script setup scripts can be directly used in markdown, and will only affects current page -->
<script setup lang="ts">
const final = {
  x: 200,
  y: 0,
  rotate: 0,
  scale: 1.5,
  opacity: 0.35,
  transition: {
    type: 'spring',
    damping: 10,
    stiffness: 20,
    mass: 2
  }
}
const finalb = {
  x: 235,
  y: 5,
  rotate: 0,
  scale: 1.5,
  opacity: 0.35,
  transition: {
    type: 'spring',
    damping: 10,
    stiffness: 20,
    mass: 2
  }
}
const finals = {
  x: 210,
  y: 5,
  rotate: 0,
  scale: 0.5,
  transition: {
    type: 'spring',
    damping: 10,
    stiffness: 20,
    mass: 2
  }
}
</script>

<div
  v-motion
  :initial="{ x: -80,y:-400, opacity: 0}"
  :enter="{ x: 200,y:-120, opacity: 1, transition: { delay: 2000, duration: 1000 } }">
  <span font-size="1em">📈</span>
</div>

<div
  v-motion
  :initial="{ x: -80,y:-400, opacity: 0}"
  :enter="{ x: 350,y:-150, opacity: 1, transition: { delay: 2000, duration: 1000 } }">
  <span font-size="1em">🖥️</span>
</div>

<div
  v-motion
  :initial="{ x: -80,y:-400, opacity: 0}"
  :enter="{ x: 285,y:-50, opacity: 1, transition: { delay: 2000, duration: 1000 } }">
  <p class="text-blue-700" size="24px">ⓘ</p> 
</div>


<div
  v-motion
  :initial="{ x: -80,y:-10, opacity: 0}"
  :enter="{ x: 250,y:-150, opacity: 1, transition: { delay: 2400, duration: 1000 } }">
  <span style="color:orange" font-size="1em">Data Science</span>
</div>

<div
  v-motion
  :initial="{ x:35, y: 40, opacity: 0}"
  :enter="{ x:700,y: -100, opacity: 1, transition: { delay: 3500 } }">

[Learn More](https://www.amazon.com/Data-Science-Handbook-Field-Cady/dp/1119092949/ref=sr_1_6?crid=3W248VBBRKKJ2&keywords=data+science+handbook&qid=1704913744&sprefix=data+science+handbook%2Caps%2C76&sr=8-6)

</div>

</p>



<!--
You can have `style` tag in markdown to override the style for the current page.
Learn more: https://sli.dev/guide/syntax#embedded-styles 
-->

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 25%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

---
transition: fade-out
---
# What is Data Science?
<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 25%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}


</style>


Key components of data science include:

<v-clicks>

1. **Data Collection**: Gathering data from various sources, which can be structured (e.g., databases) or unstructured (e.g., text, images, sensor data).

2. **Data Cleaning and Preprocessing**: Preparing the data for analysis by handling missing values, outliers, and ensuring data quality.

3. **Data Analysis**: Applying statistical and computational techniques to explore, analyze, and model the data, often using programming languages like Python or R.

4. **Data Visualization**: Creating meaningful visual representations of data through charts, graphs, and dashboards to facilitate better understanding and communication of insights.

5. **Machine Learning**: Developing and applying machine learning algorithms to build predictive models, classification systems, or recommendation systems.

</v-clicks>

---
transition: fade-out
---
# What is Data Science?
<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 25%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

Key components of data science include:

<v-clicks>

6. **Data Interpretation**: Drawing actionable conclusions from data analysis, often to inform business decisions, optimize processes, or address specific problems.

7. **Domain Expertise**: Combining data expertise with domain-specific knowledge to generate valuable insights tailored to specific industries or applications.

</v-clicks>

<v-clicks>

**Data science** is an interdisciplinary field that combines various techniques, processes, algorithms, and systems to extract valuable insights and knowledge from data. It involves collecting, cleaning, analyzing, visualizing, and interpreting data to make informed decisions and solve complex problems.

**Data scientists** work with large and complex datasets to uncover patterns, trends, and hidden insights that can drive business growth, scientific discoveries, and decision-making across various domains such as finance, healthcare, marketing, and more. The field of data science continues to evolve rapidly, incorporating advancements in technology, data management, and machine learning to harness the power of data for practical purposes.
</v-clicks>

---
transition: fade-out
---
# What is the course all about?
<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 25%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

Our course provides an introduction to modeling and machine learning methods.


<center>
<img src='https://i.imgur.com/1GlG4mx.png' width='700px'/>
<figcaption> </figcaption></center>


---
transition: slide-up
level: 2
---

# Course Structure
<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 25%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

## This course is presented in five modules:

<v-clicks>

|     |     |
| --- | --- |
| <kbd><b>Module 1</b>: Managing, Manipulating and Generating Data</kbd> |
| <kbd><b>Module 2</b>: Describing Data</kbd>|
| <kbd><b>Module 3</b>: Introduction to Modeling - Regression</kbd> | 
| <kbd><b>Module 4</b>: Introduction to Modeling - Classification</kbd> | 
| <kbd><b>Module 5</b>: Unsupervised Learning - Clustering</kbd> | 

</v-clicks>

<!-- https://sli.dev/guide/animations.html#click-animations -->
<img
  v-click
  class="absolute -bottom-12 -left-7 w-80 opacity-50"
  src="https://sli.dev/assets/arrow-bottom-left.svg"
  alt=""
/>
<p v-after class="absolute bottom-20 left-45 opacity-30 transform -rotate-40">For more info</p>

<p v-if="$slidev.nav.clicks === 6">

<div
  v-motion
  :initial="{ x:800, y: -250, opacity: 0}"
  :enter="{ x:10,y:100, opacity: 1, transition: { delay: 500 } }"
  :transition="{
    type: 'spring',
    damping: 5,
    stiffness: 10,
    mass: 20}">

[<font color='navy'> Check the Schedule</font>](https://github.com/dvasiliu/Intro-to-Data-Science)

</div>

</p>

---
layout: image-right
image: https://source.unsplash.com/collection/94734566/1920x1080
---

# Code

For coding, we use Python programming and specialized libraries. The following is a tiny example that does not involve any library import.

```python {none|1-2|4|4-9|all|}
A = ['red','orange','blue','green','yellow']
B = ['apple','carrot','peach','mango']

def f(A,B):
  l = []
  for x in A:
    for y in B:
      l.append(x+' '+y)
  return l
```

<arrow v-click="[2, 3]" x1="395" y1="420" x2="150" y2="270" color="red" width="3" arrowSize="1" />
<p v-click="[2, 3]" class="absolute bottom-23 left-100 opacity-90" color="red">function definition </p>

<p v-if="$slidev.nav.clicks === 4">
<div
  v-motion
  :initial="{ x:800, y: -250, opacity: 0}"
  :enter="{ x:10,y:100, opacity: 1, transition: { delay: 500 } }"
  :transition="{
    type: 'spring',
    damping: 5,
    stiffness: 5,
    mass: 10}">

<font color='navy' size=6px>What does this code do?</font>
</div>
</p>

<style>
.footnotes-sep {
  @apply mt-20 opacity-10;
}
.footnotes {
  @apply text-sm opacity-75;
}
.footnote-backref {
  display: none;
}
</style>

---
transition: fade-out
preload: false
clicks: 4
---
# What are variables?
<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 25%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

We can imagine that variables are measurements or attributes.

<v-click>
    <img
      v-motion
      :initial="{ x: 800, y: -100, scale: 0.5, rotate: -50}"
      :enter="final1"
      class="absolute top-0 left-20 right-0 bottom-0"
      src="https://i.imgur.com/dTBpAGr.png"
      alt=""
    />
</v-click>


<v-click>
    <img
      v-motion
      :initial="{ x: -200, y: -100, scale: 0.5, rotate: -50 }"
      :enter="final2"
      class="absolute top-0 left-0 right-0 bottom-0"
      src="https://i.imgur.com/7W9S0GB.png"
      alt=""
    />
</v-click>

<v-click>
    <img
      v-motion
      :initial="{ y: 500, x: -100, scale: 4 }"
      :enter="final3"
      class="absolute top-20 left-0 right-20 bottom-0"
      src="https://i.imgur.com/VTXXLFb.png"
      alt=""
    />
</v-click>

<v-click>
    <img
      v-motion
      :initial="{ x: 600, y: 400, scale: 2, rotate: 100 }"
      :enter="final4"
      class="absolute top-0 left-0 right-0 bottom-0"
      src="https://i.imgur.com/ApgRbw3.png"
      alt=""
    />
</v-click>


<!-- vue script setup scripts can be directly used in markdown, and will only affects current page -->
<script setup lang="ts">
const final1 = {
  x: 10,
  y: 65,
  rotate: 0,
  scale: 0.4,
  opacity: 1,
  contrast: 2.5,
  transition: {
    type: 'spring',
    damping: 10,
    stiffness: 20,
    mass: 2
  }
}
const final2 = {
  x: 118,
  y: 140,
  rotate: 0,
  scale: 0.35,
  opacity: 1,
  transition: {
    type: 'spring',
    damping: 10,
    stiffness: 20,
    mass: 2
  }
}
const final3 = {
  x: 140,
  y: 135,
  rotate: 0,
  scale: 0.3,
  opacity: 1,
  transition: {
    type: 'spring',
    damping: 10,
    stiffness: 20,
    mass: 2
  }
}
const final4 = {
  x: 230,
  y: 305,
  rotate: 0,
  scale: 0.3,
  opacity: 1,
  transition: {
    type: 'spring',
    damping: 10,
    stiffness: 20,
    mass: 2
  }
}
</script>

---
transition: fade-out
---
# Central Tendency
<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 25%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

The idea is that we want to find what is "typical" for a data set.

What are the differences between the two following data sets?


<v-clicks>

<font size=8px>1, 2, 3, 4, 4, 4, 5</font>

<br/>

<font size=8px>1, 2, 3, 4, 4, 4, 5000</font>
</v-clicks>

<arrow v-click="[4, 5]" x1="595" y1="350" x2="420" y2="300" color="red" width="3" arrowSize="1" />
<p v-click="[4, 5]" class="absolute bottom-40 left-150 opacity-90" color="red">What is the difference between the two samples? </p>


<p v-click class="absolute bottom-20 text-indigo-600"><font size=5px>What measures of central tendency are describing the data well?</font></p>

---
transition: fade-out
preload: false
clicks: 2
---
# Histograms
<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 25%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>
Histograms show the overall distribution, how frequent is data ocurring in certain intervals.



<p v-if="$slidev.nav.clicks ===1">
    <img
      v-motion
      :initial="{ x: 600, y: 400, scale: 0.5, rotate: 100, opacity: 0.2 }"
      :enter="final5"
      class="absolute top-0 left-0 right-0 bottom-0"
      src="https://i.imgur.com/9hMQw09.png"
      alt=""
    />
</p>


<v-click>
<img
      v-motion
      :initial="{ x: 600, y: 400, scale: 0.5, rotate: 100, opacity: 0.2 }"
      :enter="final6"
      class="absolute top-0 left-0 right-0 bottom-0"
      src="https://i.imgur.com/vmGK3mI.png"
      alt=""
    />
</v-click>

<script setup lang="ts">
const final5 = {
  x: -50,
  y: 38,
  rotate: 0,
  scale: 0.7,
  opacity: 1,
  contrast: 2.5,
  transition: {
    type: 'spring',
    damping: 10,
    stiffness: 20,
    mass: 2
  }
}

const final6 = {
  x: 400,
  y: 100,
  rotate: 0,
  scale: 0.8,
  opacity: 1,
  contrast: 2.5,
  transition: {
    type: 'spring',
    damping: 10,
    stiffness: 20,
    mass: 2
  }
}
</script>


---
transition: fade-out
preload: false
clicks: 1
---
# Histograms
<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 25%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>
The shape of the distribution matters for estimating probability values.

<p v-if="$slidev.nav.clicks ===1">
    <img
      v-motion
      :initial="{ x: 600, y: 400, scale: 0.5, rotate: 100, opacity: 0.2 }"
      :enter="final5"
      class="absolute top-0 left-0 right-0 bottom-0"
      src="https://i.imgur.com/POPqkGO.png"
      alt=""
    />
</p>



<script setup lang="ts">
const final5 = {
  x: 100,
  y: 70,
  rotate: 0,
  scale: 0.8,
  opacity: 1,
  contrast: 2.5,
  transition: {
    type: 'spring',
    damping: 10,
    stiffness: 20,
    mass: 2
  }
}

const final6 = {
  x: 320,
  y: 38,
  rotate: 0,
  scale: 0.7,
  opacity: 1,
  contrast: 2.5,
  transition: {
    type: 'spring',
    damping: 10,
    stiffness: 20,
    mass: 2
  }
}
</script>

---
transition: fade-out
---
# Variability Measures
<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 25%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

We want to know how spread the data is from its center or typical value. 

If the data is a continuous variable and the center is defined to be the mean, then variance and standard deviation are measures of variability:

<v-clicks>
<div><font size=5px> Variance</font></div>

$$\large \text{Var}(X):= \frac{\sum (X_i-\mu)^2}{N}$$

Here $\mu$ is the mean of the random variable, and $N$ is the size of the population.

<div><font size=5px>Sample Variance</font></div>

$$\large \text{Var}(x):= \frac{\sum (x_i-\bar{x})^2}{n-1}$$

Here $\bar{x}$ is the mean of the sample, and $n$ is the sample size. 

</v-clicks>


---
transition: fade-out
---
# Variability Measures
<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 25%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

The standard deviation can help us create a useful metric for variable studied, and also scale its values.

<v-clicks>

The sample standard deviation is:

$$\Large s_x:= \sqrt{\frac{\sum (x_i-\bar{x})^2}{n-1}}$$

Therefore, a scaler can be achieved via $z$-score:

$$\Large z_{x_i} = \frac{x_i-\bar{x}}{s_x}$$

This works in many situations, provided the standard deviation is not zero.

<p class="text-indigo-600"><font color='red' size=6px>Critical Thinking:</font>What would the data look like if the standard deviation is exactly zero?</p>

</v-clicks>


---
transition: fade-out
---
# Coefficient of Variation
<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 25%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

For the data below we want to find a solution that is less biased when highlighting differences.
<v-clicks>

<font size=8px class='text-indigo-600'>1, 2, 3, 4, 4, 4, 5</font>

<br/>

<font size=8px class='text-red-600'>1, 2, 3, 4, 4, 4, 5000</font>


The coefficient of variation may shed some light:

$$\large \frac{s_x}{\bar{x}}$$

For the first sample this is $0.388$, and for the second sample this is $2.439.$

</v-clicks>

---
transition: fade-out
---
# Percentiles and Quartiles
<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 25%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>
Main point: we want to analyze measures resistant to outliers.

<v-clicks>

<p size=6px class="text-indigo-700"><font size=6px class="text-red-600">Percentiles:</font> The p-th percentile is a value x in the metric of a variable (that is at least interval level) such that p% of the values of the variable are below x.</p>

<p size=6px class="text-indigo-700"><font size=6px class="text-red-600">Median:</font> The median is the 50-th percentile.</p>

<p size=6px class="text-indigo-700"><font size=6px class="text-red-600">Quartiles:</font> Q1 is th 25-th percentile, and Q3 is the 75-th percentile.</p>

<p size=6px class="text-indigo-700"><font size=6px class="text-red-600">IQR (Inter-quartile Range):</font> Q3 - Q1.</p>

<p size=6px class="text-indigo-700"><font size=6px class="text-red-600">Outliers:</font> Any value that is 1.5xIQR below Q1 or 1.5xIQR above Q3.</p>

Can we provide a summary of a variable based on these ideas? Yes, we can create boxplots.

</v-clicks>

---
transition: fade-out
clicks: 1
---
# Boxplots and Outliers
<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 25%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

Consider the data sample:

1.5, 1.75, 2, 2.13, 2.42, 2.61, 3.1, 3.1, 3.4, 3.98, 3.99

The boxplot is:


<p v-if="$slidev.nav.clicks ===1">
    <img
      v-motion
      :initial="{ x: 600, y: 400, scale: 0.5, rotate: 100, opacity: 0.2 }"
      :enter="final5"
      class="absolute top-0 left-0 right-0 bottom-0"
      src="https://i.imgur.com/v7ysndm.png"
      alt=""
    />
</p>

<script setup lang="ts">
const final5 = {
  x: 350,
  y: 230,
  rotate: 0,
  scale: 1.8,
  opacity: 1,
  contrast: 2.5,
  transition: {
    type: 'spring',
    damping: 10,
    stiffness: 20,
    mass: 2
  }
}
</script>


---
transition: fade-out
clicks: 2
---
# Boxplots and Outliers
<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 25%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

For using boxplot from Matplotlib the clarification is here:


<p v-if="$slidev.nav.clicks ===1">
    <img
      v-motion
      :initial="{ x: 600, y: 400, scale: 0.01, rotate: 120, opacity: 0.2 }"
      :enter="final5"
      class="absolute top-0 left-0 right-0 bottom-0"
      src="https://i.imgur.com/qEQQhKV.png"
      alt=""
    />
</p>

<script setup lang="ts">

const final5 = {
  x: 20,
  y: 50,
  rotate: 0,
  scale: 0.6,
  opacity: 1,
  contrast: 2.5,
  transition: {
    type: 'spring',
    damping: 10,
    stiffness: 20,
    mass: 2
  }
}
</script>

<p v-if="$slidev.nav.clicks === 1">

<div
  v-motion
  :initial="{ x:0, y:340, opacity: 0}"
  :enter="{ x:650,y:340, opacity: 1, transition: { delay: 2000 } }"
  :transition="{
    type: 'spring',
    damping: 2,
    stiffness: 1,
    mass: 2}">

[<font color='navy'> Reference </font>](https://www.nickmccullum.com/python-visualization/boxplot/)

</div>

</p>



---
transition: fade-out
clicks: 2
---
# Bounds Justification

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 25%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}
</style>

The justification for the "minimum" and the "maximum" values in the case of boxplots is drawn from a normal distribution.

<p v-if="$slidev.nav.clicks ===1">
    <img
      v-motion
      :initial="{ x: 600, y: 400, scale: 0.01, rotate: 100, opacity: 0.2 }"
      :enter="final5"
      class="absolute top-0 left-0 right-0 bottom-0"
      src="https://i.imgur.com/pSaIQpM.png"
      alt=""
    />
</p>

<script setup lang="ts">
const final5 = {
  x: -50,
  y: -30,
  rotate: 0,
  scale: 0.5,
  opacity: 1,
  contrast: 2.5,
  transition: {
    type: 'spring',
    damping: 10,
    stiffness: 20,
    mass: 2
  }
}
</script>

<p v-if="$slidev.nav.clicks === 1">

<div
  v-motion
  :initial="{ x:0, y:340, opacity: 0}"
  :enter="{ x:650,y:340, opacity: 1, transition: { delay: 2000 } }"
  :transition="{
    type: 'spring',
    damping: 2,
    stiffness: 1,
    mass: 2}">

[<font color='navy'> Reference </font>](https://towardsdatascience.com/create-and-customize-boxplots-with-pythons-matplotlib-to-get-lots-of-insights-from-your-data-d561c9883643)

</div>

</p>
