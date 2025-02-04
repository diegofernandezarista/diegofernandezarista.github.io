---
title: "Bias Variance Trade-off"
date: 2025-01-27T22:53:58+05:30
draft: false
github_link: "https://github.com/diegofernandezarista"
author: "Diego Fernandez Arista"
tags:
  - Bias
  - Variance
  - Underfitting
  - Overfitting
image: /images/post_bias_variance_tradeoff.png
description: ""
toc: 
---

---

When it comes to the 𝗯𝗶𝗮𝘀-𝘃𝗮𝗿𝗶𝗮𝗻𝗰𝗲 𝘁𝗿𝗮𝗱𝗲𝗼𝗳𝗳 and 𝗶𝘁𝘀 𝗿𝗲𝗹𝗮𝘁𝗶𝗼𝗻𝘀𝗵𝗶𝗽 𝘄𝗶𝘁𝗵 𝘂𝗻𝗱𝗲𝗿𝗳𝗶𝘁𝘁𝗶𝗻𝗴 𝗮𝗻𝗱 𝗼𝘃𝗲𝗿𝗳𝗶𝘁𝘁𝗶𝗻𝗴 𝗶𝗻 𝗺𝗮𝗰𝗵𝗶𝗻𝗲 𝗹𝗲𝗮𝗿𝗻𝗶𝗻𝗴, I sometimes need a few seconds to fully connect the dots in my mind. 🔄🧠 Has this ever happened to you? 🤔 If your answer is yes, let me share you how I see it and help myself. I always try to relate these concepts to real-life examples. I hope this approach benefits you too. 💡

𝗕𝗶𝗮𝘀 ⚖️

» To start, what exactly is bias in everyday life? Bias refers to an inclination toward something without considering all that is at stake. For instance, if you and your friends always prefer a certain type of food based on past experiences, you might ignore other great options simply because you’re used to your favorite dish. And, let me tell you, friend, that’s bias. 🍔🍕

» Now, what about bias in analytics, and how is it connected to underfitting? Imagine you and your friends are the machine learning model trying to predict how good a dish at a restaurant is. If you focus only on a few factors, such as price or ingredients, while ignoring key aspects like customer reviews, the chef’s experience, the restaurant’s location, and others, your predictions could be biased. This happens because the model oversimplifies the problem, making it unable to learn enough from the training data. As a result, if the features you’re using to judge new dishes are limited or less important, this leads to high bias and, consequently, underfitting. 🧩❓

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ![Bias Example](/images/bias_variance_tradeoff/1.png)

𝗩𝗮𝗿𝗶𝗮𝗻𝗰𝗲 📈

» What about variance in everyday life? Variance refers to differences in how people respond to the same situation. For example, imagine you and your friends watch the same movie. If most of you think it’s great, the variance is low. But if one person loves it, another dislikes it, and someone else has mixed feelings, the variance is high. 🎬🍿

» Now, let’s connect this to variance in analytics and how it relates to overfitting. Imagine you and your friends are the machine learning model trying to predict how good a movie is. If you focus on every little detail from the movies you like—such as specific phrases in the reviews, ratings, one-off opinions, and others—your predictions may work perfectly for those cases and similar ones. However, when faced with new movies that don’t match those patterns, your predictions become inconsistent and unreliable. And that, my friend, is overfitting because you, as a model, are too rooted in the characteristics of the training data—in this case, the detailed features you focused on from the movies you like. In other words, the model becomes overly sensitive to small details or noise. 🎯🔍

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;![Variance Example](/images/bias_variance_tradeoff/2.png)

Was this approach helpful for you? 🤔💡 I hope so! If you have any questions or want to discuss it further, please don't hesitate to contact me ✉️.