---
layout: post
title:  Demystifying Machine Learning in Climate Science
description: 
tags: [climate, predictability, subseasonal, forecasting]
comments: true
category: blog
date: 2022-10-23
img: SC_NN-analogy_pie-recipe_thumbnail.png
authors: 
- Marybeth Arcodia
---

<i>Robots are taking over the world!!!</i>
<br><br>
Fortunately (or unfortunately, depending on your feelings toward robots), artificial intelligence (AI) has provided groundbreaking advancements and improvements to our lives without involving evil-robots-taking-over-the-world. In fact, misconceptions about AI often result in fear, despite AI being used all around us: filtering of your inbox to spam, your Amazon Alexa or Google Home, facial recognition to unlock your phone, fraud detection for your bank account, the list goes on and on.
<br>
<h2>AI in Climate Science</h2>

Not only has AI improved technologies in everyday life, but it is also making great strides in the climate science field. Particularly useful in the scientific community is machine learning, a subset of AI which involves training a model to “learn” via mathematical calculations to reduce its errors. Machine learning could instead be called “algorithm optimization” which would better encapsulate the mathematical and statistical processes involved, but that just isn’t as catchy.
<br><br>
While applications of machine learning in atmospheric science can date back to the 1960s[<sup>1</sup>](https://journals.ametsoc.org/view/journals/apme/3/6/1520-0450_1964_003_0718_aaoalt_2_0_co_2.xml), recent improvements in data quality and availability, processing power, and computer science techniques have catapulted machine learning to the forefront of data science methods. Recent applications include global weather prediction[<sup>2</sup>](https://agupubs.onlinelibrary.wiley.com/doi/full/10.1029/2020MS002109), extreme event detection[<sup>3</sup>](https://www.nature.com/articles/s41586-019-0912-1), data reconstruction[<sup>4</sup>](https://www.nature.com/articles/s41561-020-0582-5), rapid intensification of hurricanes[<sup>5</sup>](https://ui.adsabs.harvard.edu/abs/2021AGUFM.H35M1182K/abstract), and subseasonal-to-decadal climate predictability[<sup>6</sup>](https://agupubs.onlinelibrary.wiley.com/doi/10.1029/2020GL092092), which you may remember from our [weather pattern pie](https://seasonedchaos.github.io/What-Can-the-Tropics-Tell-Us-About-Next-Weeks-Weather/). 
<br><br>
Speaking of pies, imagine that your grandma made the best key lime pie and you wanted to recreate it, but she keeps the recipe a secret. You try to figure out which ingredients you need and how much of each to use. So, you take your best guess at the ingredients and ratios needed and bake a key lime pie. But when you taste it, you realize it needs a bit more cream. You start over and add cream, but now realize you need to take out some sugar. You bake pies over and over again, each time getting just a little closer to grandma’s perfect pie until FINALLY you find the perfect recipe for a key lime pie that tastes just like Grandma’s! 
<br><br>
This fine-tuning recipe process is similar to how artificial neural networks, a frequently used type of machine learning, work. Originally inspired by a biological neuron network, an artificial neural network takes in information (ingredients), passes the information through a series of processing steps (combining ingredients in certain ratios), and gives an output (pie). The neural network model is trained by comparing the network’s predicted output to the actual value (ie the truth) and stepping backwards through the model to correct its errors. This is an iterative process that is repeated many times until the network is optimized to make a good prediction.  
<br><br>
<img src="/assets/img/SC_NN-analogy_pie-recipe.png" width="100%">
<br><sub><i>The process of fine-tuning your Grandma's recipe can be used as an analogy for a neural network. (And yes, the Seasoned Chaos team may have a pie obsession...)</i></sub>
<br><br>
<h2>Opening the Oven (Black Box)</h2>

As scientists, we not only want a model to make a good prediction, but we want to know why it made a good prediction. After all, a machine learning model is only as smart as the scientists designing it. Scientists have historically been cautious to use ML as it is commonly thought to be a black box. ML procedures were considered "mysterious" in the sense that they couldn't be replicated or interpreted with only basic knowledge of mathematics/physics. But this is no longer the case! We use interpretable models and apply explainability methods to allow us to understand precisely how an ML model makes its predictions. These eXplainable Artificial Intelligence, or XAI, methods highlight important patterns for the predictions which allow the user to understand the network’s decision making process[<sup>7</sup>](https://link.springer.com/chapter/10.1007/978-3-031-04083-2_16)<sup>,</sup>[<sup>8</sup>](https://agupubs.onlinelibrary.wiley.com/doi/10.1029/2020GL092092). We use explainable and trustworthy machine learning techniques to:
<br><br>
<b>1. Gauge Trust in Model</b>
<br><br>
Did the model actually learn something real or did it just get lucky? We want to ensure 
that the model is making a good prediction for the right reasons, or figure out why it was wrong. Using XAI, we can learn what input features the model deemed important and verify the network’s prediction strategy.
<br><br>
<b>2. Learn New Science</b>
<br><br>
Once we have established trust in our model, we can analyze what the model learned. This can help us discover new sources of predictability, disentangle signals from the [chaotic noise](https://seasonedchaos.github.io/The-More-We-Learn-the-Less-We-Know-An-Introduction-to-Chaos/), and find relationships within the climate system we didn’t know were there. 
<br><br>
<b>3. Optimize</b>
<br><br>
Simply put, using ML can help us do science better and faster. We can fine tune our approaches and process large amounts of data efficiently. This can help with data-intensive calculations that are often involved in climate processes, such as tracking hurricanes, identifying [atmospheric blocks](https://seasonedchaos.github.io/Traffic-Jams-and-Club-Sandwiches-in-the-Atmosphere-An-Overview-of-Blocking/), and sifting through large amounts of climate model data. 
<br><br>
It is important to remember that ML is another tool in a climate scientist’s toolbox. Many standard approaches using statistics, dynamics, and theory for scientific analysis are still effective and valid, and machine learning is an exciting and innovative addition. For example, in a [previous post](https://seasonedchaos.github.io/What-Can-the-Tropics-Tell-Us-About-Next-Weeks-Weather/), we discussed research using these approaches to show how the state of the atmospheric and oceanic states of the tropical Pacific can affect weather in the United States on subseasonal (2 week - 2 month) timescales. In my current research, we study a similar problem by using artificial neural networks to make subseasonal predictions of U.S. rainfall using the state of the tropics. By applying the XAI techniques, we can then determine which features in the tropics the model deemed important for its prediction (such as the El Niño/La Niña region, the MJO region, and perhaps regions we hadn’t looked at before). We are also able to quantify how confident the network was in its prediction to identify more predictable time periods, known as forecasts of opportunity. We can assess how these predictable time periods change over long periods of time and how these predictable states may change in the future[<sup>8</sup>](https://doi.org/10.1029/2022GL098663). Machine learning allows scientists to investigate complex and interconnected climate phenomena in a digestible way to push scientific knowledge farther than ever before. 
<br><br>
Today, we can open the black box and understand what and how ML models have learned. ML is not robots taking over and it is not magic. Instead, it is a powerful technique that can help scientists ultimately learn new science, perhaps while enjoying a perfectly baked slice of key lime pie. 
<br><br>
<div style="text-align: right"><i> Written by: Marybeth Arcodia</i></div>
<div style="text-align: right"><i> Graphics credit to: Kelsey Malloy (+ pie graphic descends from Kayla Besong's work)</i></div>
<br><br>
For additional information, [check out these great YouTube videos](https://sites.google.com/view/barnesgroup-csu/scicomm?authuser=0) on explainable machine learning in climate science.
<br>
And check out [this in-depth tutorial for applied machine learning for climate scientists](https://zenodo.org/record/6686879#.Y024BezML0o) including step-by-step example code.
<br><br>
Footnotes:
<br>
[<sup>1</sup>](https://journals.ametsoc.org/view/journals/apme/3/6/1520-0450_1964_003_0718_aaoalt_2_0_co_2.xml)Glahn, H. R. (1964). An Application of Adaptive Logic to Meteorological Prediction, Journal of Applied Meteorology and Climatology, 3(6), 718-725.
<br>
[<sup>2</sup>](https://agupubs.onlinelibrary.wiley.com/doi/full/10.1029/2020MS002109)Weyn, J. A., Durran, D. R., & Caruana, R. (2020). Improving data-driven global weather prediction using deep convolutional neural networks on a cubed sphere. Journal of Advances in Modeling Earth Systems, 12, e2020MS002109.
<br>
[<sup>3</sup>](https://www.nature.com/articles/s41586-019-0912-1)Reichstein, M., Camps-Valls, G., Stevens, B. et al. (2019). Deep learning and process understanding for data-driven Earth system science. Nature 566, 195–204.
<br>
[<sup>4</sup>](https://www.nature.com/articles/s41561-020-0582-5)Kadow, C., Hall, D.M. & Ulbrich, U. (2020). Artificial intelligence reconstructs missing climate information. Nat. Geosci. 13, 408–413.
<br>
[<sup>5</sup>](https://ui.adsabs.harvard.edu/abs/2021AGUFM.H35M1182K/abstract)Ko, M. C., Kubat, M., Gopalakrishnan, S., & Chen, X. (2021). The Development of a Consensus Machine Learning Model for Hurricane Rapid Intensity (RI) Forecasts with Hurricane Weather Research and Forecast (HWRF) Data. AGU Fall Meeting Abstracts.
<br>
[<sup>6</sup>](https://agupubs.onlinelibrary.wiley.com/doi/10.1029/2020GL092092)Mayer, K. J., & Barnes, E. A. (2021). Subseasonal forecasts of opportunity identified by an explainable neural network. Geophysical Research Letters, 48.
<br>
[<sup>7</sup>](https://link.springer.com/chapter/10.1007/978-3-031-04083-2_16)Mamalakis, A., Ebert-Uphoff, I., Barnes, E. (2022). Explainable Artificial Intelligence in Meteorology and Climate Science: Model Fine-Tuning, Calibrating Trust and Learning New Science. Invited book chapter.
<br>
[<sup>8</sup>](https://agupubs.onlinelibrary.wiley.com/doi/10.1029/2020GL092092)Mamalakis, A., Ebert-Uphoff, I., & Barnes, E. (2022). Neural network attribution methods for problems in geoscience: A novel synthetic benchmark dataset. Environmental Data Science, 1, E8.
<br>
