---
title: "Breast cancer Analysis using R - Machine Learning"
layout: post
date: 2019-12-5
<!--image: /assets/images/markdown.jpg -->
headerImage: false
<!-- tag:
- markdown
- components
- extra -->
category: blog
author: jamesfoster
description: Markdown summary with different options
---

## Introduction:

According to a 2018 report by the World Health Organization, cancer is a leading cause of death worldwide, breast cancer is also the second most common cancer worldwide. So, we decided to study the breast cancer Wisconsin dataset, using different methods of classiﬁcation in ML and comparing them to determine the appropriate one. This analysis will be used to determine whether a certain tumor is benign or malignant. We have chosen R language for the implementation.

## Why R:

R is an open source programming language used for statistical computations, data analysis and graphical representation of data. It is the best choice in our case as it has many packages useful for ML & statistical processes, also it has many advantages including data wrangling and data visualization. 


## Our Data set:

<a href="https://www.kaggle.com/uciml/breast-cancer-wisconsin-datax">Wisconsin Data set</a> for Breast cancer classification is a good classifier tool for our machine learning project, 
Features are computed from a digitized image of a fine needle aspirate (FNA) of a breast mass. They describe characteristics of the cell nuclei present in the image.



<hr>

# Machine Learning Model

## 1. Pre-Processing:
The dataset we are working on consists of 569 examples and 32 features.
To avoid irrelevant or redundant features that may have a negative effect on the accuracy of the classifier, we have used **feature selection** by ordering features by their importance, then we have neglected the least important ones.


<hr>

## 2. Plotting Importance
<img src="https://amanybahaaeldin.github.io/assets/images/Importance.png">
<figcaption class="caption">Importance</figcaption>


<hr>



---
## 3. Classification Methods:
In machine learning, classification is the process of identifying to which of a set of classes a new example belongs. There are several methods of classification but we have chosen the most appropriate ones to our dataset which are:
<ol>
<li>Decision Tree</li>
<li>Naive Bayes</li>
<li>KNN</li>
</ol>

## 3.1. Decision Tree
A Decision Tree is a supervised Machine Learning algorithm wherein each node represents a feature, the link between the nodes represents a decision and each leaf node represents an outcome.
It's considered to be one of the most useful ML algorithms, also it is suitable for our dataset as it is used extensively for diagnosis of diseases such as breast cancer, ovarian cancer, heart sound diagnosis, etc. 
<img src="https://amanybahaaeldin.github.io/assets/images/Decision Tree.png">
<figcaption class="caption">Decision Tree</figcaption>



<hr>


## 3.2. Naive Bayes
The Naive Bayes classifiers are working based on the Bayes' theorem, which describes the probability of an event based on prior knowledge of conditions be related of conditions to the event.
Bayes' Theorem: P(A|B) = (P(B|A) * P(A)) / P(B)
<img src="https://amanybahaaeldin.github.io/assets/images/Naive Bayes.png">
<figcaption class="caption">Naive Bayes</figcaption>
<ol>
<li>Accuracy = 93.8%</li>
<li>Sensitivity = 95.69%</li>
<li>Specificity = 92.67%</li>
</ol>


<hr>


## 3.3. KNN 
In k-NN classification, the output is a class membership. An object is classified by a plurality vote of its k nearest neighbors.
<img src="https://amanybahaaeldin.github.io/assets/images/KNN.png"><ol>
<figcaption class="caption">KNN</figcaption>

<li>Accuracy = 96.67%</li>
<li>Sensitivity = 99.47%</li>
<li>Specificity = 92.29%</li>
</ol>

<hr><hr>

## 4. k-Fold Cross-Validation

Cross-Validation is a statistical method used to estimate the skill of machine learning models,
The procedure has a single parameter called k that refers to the number of groups that a given data sample is to be split into.
It involves randomly dividing the set of examples into k groups, or folds, of approximately equal size. The first fold is treated as a validation set, and the method is fit on the remaining k − 1 folds.
The choice of k is usually 5 or 10, but there is no formal rule. As k gets larger, the difference in size between the training set and the resampling subsets gets smaller. As this difference decreases, the bias of the technique becomes smaller.

# Conclusion



After applying the 3 methods with k-fold cross-validation, we have found that the most suitable one for our datset is the **kNN method** as it has the greatest accuracy. 


---

<!-- 
## Side-by-side

Like the [Medium](https://medium.com/) component.

**Image** on the left and **Text** on the right:

{% highlight html %}
<div class="side-by-side">
    <div class="toleft">
        <img class="image" src="{{ site.url }}/{{ site.picture }}" alt="Alt Text">
        <figcaption class="caption">Photo by John Doe</figcaption>
    </div>

    <div class="toright">
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
    </div>
</div>
{% endhighlight %} -->

<!-- <div class="side-by-side">
    <div class="toleft">
        <img class="image" src="{{ site.url }}/{{ site.picture }}" alt="Alt Text">
        <figcaption class="caption">Photo by John Doe</figcaption>
    </div>

    <div class="toright">
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
    </div>
</div> -->
<!-- 
**Text** on the left and **Image** on the right:

{% highlight html %}
<div class="side-by-side">
    <div class="toleft">
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
    </div>

    <div class="toright">
        <img class="image" src="{{ site.url }}/{{ site.picture }}" alt="Alt Text">
        <figcaption class="caption">Photo by John Doe</figcaption>
    </div>
</div>
{% endhighlight %}

<div class="side-by-side">
    <div class="toleft">
        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
    </div>

    <div class="toright">
        <img class="image" src="{{ site.url }}/{{ site.picture }}" alt="Alt Text">
        <figcaption class="caption">Photo by John Doe</figcaption>
    </div>
</div>

--- -->

<!-- ## Star

You can give evidence to a post. Just add the tag to the markdown file.

{% highlight raw %}
star: true
{% endhighlight %}

---

## Especial Breaker

You can add a especial *hr* to your text.

{% highlight html %}
<div class="breaker"></div>
{% endhighlight %}
 -->
<div class="breaker"></div>

---

<!-- ## Spoiler

You can add an especial hidden content that appears on hover.

{% highlight html %}
<div class="spoiler"><p>your content</p></div>
{% endhighlight %}

<div class="spoiler"><p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p></div>

---

## Gist

You can add Gists from github.

{% highlight raw %}
{ % gist sergiokopplin/91ff4220480727b47224245ee2e9c291 % }
{% endhighlight %}

{% gist sergiokopplin/91ff4220480727b47224245ee2e9c291 %}

---
 -->
<!-- ## Codepen

You can add Pens from Codepen.

{% highlight html %}
<p data-height="268" data-theme-id="0" data-slug-hash="gfdDu" data-default-tab="result" data-user="chriscoyier" class='codepen'>
    See the Pen <a href='http://codepen.io/chriscoyier/pen/gfdDu/'>Crappy Recreation of the Book Cover of *The Flame Alphabet*</a> by Chris Coyier (<a href='http://codepen.io/chriscoyier'>@chriscoyier</a>) on <a href='http://codepen.io'>CodePen</a>.
</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>
{% endhighlight %}

<p data-height="268" data-theme-id="0" data-slug-hash="gfdDu" data-default-tab="result" data-user="chriscoyier" class='codepen'>See the Pen <a href='http://codepen.io/chriscoyier/pen/gfdDu/'>Crappy Recreation of the Book Cover of *The Flame Alphabet*</a> by Chris Coyier (<a href='http://codepen.io/chriscoyier'>@chriscoyier</a>) on <a href='http://codepen.io'>CodePen</a>.</p>
<script async src="//assets.codepen.io/assets/embed/ei.js"></script>

---

## Slideshare

Add your presentations here!

{% highlight html %}
<iframe src="//www.slideshare.net/slideshow/embed_code/key/hqDhSJoWkrHe7l" width="560" height="310" frameborder="0" marginwidth="0" marginheight="0" scrolling="no" style="border:1px solid #CCC; border-width:1px; margin-bottom:5px; max-width: 100%;" allowfullscreen> </iframe>
{% endhighlight %}

<iframe src="//www.slideshare.net/slideshow/embed_code/key/hqDhSJoWkrHe7l" width="560" height="310" frameborder="0" marginwidth="0" marginheight="0" scrolling="no" style="border:1px solid #CCC; border-width:1px; margin-bottom:5px; max-width: 100%;" allowfullscreen> </iframe>

---

## Videos

Do you want some videos? Youtube, Vimeo or Vevo? Copy the embed code and paste on your post!

**Example**

{% highlight html %}
<iframe width="560" height="310" src="https://www.youtube.com/embed/r7XhWUDj-Ts" frameborder="0" allowfullscreen></iframe>
{% endhighlight %} -->

<!-- <iframe width="560" height="310" src="https://www.youtube.com/embed/r7XhWUDj-Ts" frameborder="0" allowfullscreen></iframe>

[1]: http://daringfireball.net/projects/markdown/
[2]: http://www.fileformat.info/info/unicode/char/2163/index.htm
[3]: http://www.markitdown.net/
[4]: http://daringfireball.net/projects/markdown/basics
[5]: http://daringfireball.net/projects/markdown/syntax
[6]: http://kune.fr/wp-content/uploads/2013/10/ghost-blog.jpg
 -->