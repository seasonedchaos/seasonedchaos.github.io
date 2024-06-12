---
layout: post
title: Feast Your Eyes On The North American Multi-Model Ensemble
description: At Seasoned Chaos, we've explored a smorgasbord of weather and climate topics, from predictability and chaos to teleconnections and human impacts. 
tags: [model, predictability, subseasonal, seasonal, climate, prediction]
comments: true
category: blog
date: 2024-06-12
img: insert
authors:
- Kayla Besong
---


At Seasoned Chaos, we've explored a smorgasbord of weather and climate topics, from predictability and chaos to teleconnections and human impacts. We've shared some [subseasonal](https://seasonedchaos.github.io/Things-are-getting-heated-the-science-behind-the-polar-vortex-and-stratospheric-warmings/) to [seasonal](https://seasonedchaos.github.io/2022-Hurricane-Season-Forecast/) (S2S) outlooks and, of course, there’s been plenty of pie. But there's one key dish we haven't yet brought to the table: the North American Multi-Model Ensemble, or [NMME](https://tenor.com/view/finding-nemo-anemone-awkward-cant-pronounce-gif-8178744). The NMME is a suite of <i>seasonal climate forecast</i> models from various North American centers, used for S2S forecasting.
<br><br>

<h2>A Mozzarella-Parmesan Blend?</h2>

How does a seasonal climate forecast model differ from a weather forecast model or a 'regular' climate model? It’s a mix of both. Producing a climate forecast is like aging a fine cheese such as parmesan, focusing on long-term changes in climate patterns over decades or centuries using baseline conditions like carbon dioxide levels. A weather forecast is like whipping up a fresh mozzarella, providing quick, short-term predictions of localized conditions [based on the current state](https://seasonedchaos.github.io/Mastering-Chaos-A-Spooky-Introduction-to-Data-Assimilation/) of the atmosphere.
<br><br>
Seasonal forecast models are like a blend of these cheeses, offering both short-term and long-term insights. They are initialized with the current atmospheric state and make predictions at the ‘in-between’ S2S timescale.
<br><br>

[<h2>A Mozzarella-Parmesan Blend?</h2>](https://www.foodnetwork.com/recipes/articles/feast-of-the-seven-fishes)

Each of the seven seasonal forecast models of the NMME is like a unique dish at an Italian feast, offering a distinct perspective on future conditions; each one similar, yet different to create a comprehensive spread of monthly predictions ranging 9 to 12 months in advance.
<br><br>
These models use complex equations, known as [primitive equations](https://staff.cgd.ucar.edu/islas/teaching/2_Equations.pdf) (a lot of intense math and physics), to simulate how air flows, changes phase, and interacts with the ocean, etc. This makes them <i>dynamical</i> models, differing from statistical models, a distinction we [investigated](https://seasonedchaos.github.io/CSI-SC-The-Spring-Predictability-Barrier/) a while back.
<br><br>

<h2>A Little Bit of This, a Little Bit of That</h2>

Due to scale, complexity, and computational resources, not all processes like cloud formations or ocean eddies can be fully simulated by climate models. We have to work with what we already have in the kitchen, aka use <i>parameterizations</i> to estimate the effects of these processes at each grid cell. The parameterization ‘recipe’ each model follows varies by modeling center. This diversity is a good thing! Rather than a competition on whose sauce is better, the combined multi-model ensemble (MME) approach helps smooth out biases and errors that come with predicting the future.
<br><br>

<h2>A Classic Spaghetti Plot</h2>

Our posts are as seasoned with chaos as your pasta water should be salted, heavily. That is because predicting the future, [especially at S2S timescales](https://seasonedchaos.github.io/a-personality-test-for-our-climate-system-the-basis-for-forecasting-in-between/), is challenging–a difficulty well highlighted by [Chaos Theory](https://seasonedchaos.github.io/The-More-We-Learn-the-Less-We-Know-An-Introduction-to-Chaos/). An MME not only smooths biases but also mitigates this chaos by capturing a broader range of potential future conditions. If one sauce is too salty, one is too watery, and another is too spicy, combined they are more balanced. Adding an extra layer of flavor, the models themselves have ensembles of their own! Every model is run multiple times, called an ensemble member, each with slightly varying initial conditions. 
<br><br>
To visualize our ensemble of ensembles, take a look at the [spaghetti plot](https://en.wikipedia.org/wiki/Spaghetti_plot) below of the NMME Oceanic Niño Index (ONI) forecast – a metric that describes the western Pacific SST trend, commonly used to help determine the [phase of ENSO](https://seasonedchaos.github.io/Round-1-ENSO-is-King/). 
<br><br>
The thin lines (angel hair – thinnest noodle) represent individual ensembles for each model, while the thick line of the same color (linguine – thicker noodle) shows the average of those ensembles within an individual model. The thick black line (fettuccine – thickest noodle) is the NMME, or average of all the models (linguine), showing the overall best predicted trend of future conditions. 
<br><br>
<img src="/assets/img/N34plume.dynamic.today.html" width="95%">
<br><sub><i>NMME forecast of Oceanic Niño Index, where color indicates which model and thick black line is either best estimate of observed state (before forecast initialization) or the multi-model mean (after forecast initialization).</i></sub>
<br><br>
The models show good agreement in predicting an upcoming La Niña, all trending below the -0.5&deg;C threshold. If some models predicted El Niño while others predicted La Niña, the larger spread would indicate high uncertainty/low predictability of the future.
<br><br>
While using the NMME, forecasters rely on signals from ENSO, [regimes](https://seasonedchaos.github.io/Weather-Regimes-The-Atmospheres-Preferred-Moods/), or other climate-related patterns such as those in our [weather-pattern pie](https://seasonedchaos.github.io/What-Can-the-Tropics-Tell-Us-About-Next-Weeks-Weather/) ([NAO](https://seasonedchaos.github.io/Seasoned-Chaos-presents-the-North-Atlantic-Oscillation/), [PNA](https://seasonedchaos.github.io/Teleconnection-Telenovela-Pasion-of-the-Pacific-North-American-Pattern/), [Blocking](https://seasonedchaos.github.io/Traffic-Jams-and-Club-Sandwiches-in-the-Atmosphere-An-Overview-of-Blocking/), [Monsoons](https://seasonedchaos.github.io/Part-I-A-Sprinkle-on-Monsoons/), etc.) to help predict extremes often tied to these phenomena. 
<br><br>

<h2>So What, No Ziti Now?</h2>

We all want a good, reliable forecast, like Grandma’s ziti [on our birthdays](https://ibb.co/CzK9MLX). But if you [come to me for a forecast on the day of my daughter's wedding](https://www.youtube.com/watch?v=8vwsu4-jFBw), asking if it will rain at 1 pm three months from now, we can’t grant any guarantees. The best we can offer is [guidance in the form of probabilities](https://seasonedchaos.github.io/Round-2-Welcome-to-the-Seasoned_Chaos-Casino/). 
<br><br>
When displayed in probabilistic format, NMME forecasts become highly useful on S2S timescales. Due to the combination of all the models and their ensembles, the likelihood of a given condition such as temperature being above, below, or near normal conditions becomes much more [reliable](https://journals.ametsoc.org/view/journals/clim/29/8/jcli-d-14-00862.1.xml#fig8). S2S forecasts such as these help with [emergency management and risk reduction, public health awareness, agriculture, the energy sector, and water resource management](https://journals.ametsoc.org/view/journals/clim/29/8/jcli-d-14-00862.1.xml#fig8). 
<br><br>
<img src="/assets/img/nmme_forecast_all_var.html" width="95%">
<br><sub><i>NMME probability forecast of above-, below-, and near-normal conditions for July 2024.</i></sub>
<br><br>
Will below average precipitation impact the tomato crop and, consequently, Grandma’s ziti? Will above average temperatures bring heat that makes us sweat like we're in a sit-down with the Don? 
<br><br>

<h2>Looking for Seconds?</h2>

You’re in luck, there’s plenty. The NMME products featured here (and more!) will be offered up in real-time, around the 7th of each month. In collaboration with the University of Miami and fellow beautiful science queen [Emily Becker](https://scholar.google.com/citations?user=WqWhGJEAAAAJ&hl=en), I’ll be serving up monthly forecasts of:
- An [interactive](https://nmme.earth.miami.edu/forecasts/n34plume.dynamic.today.html) and [static](https://nmme.earth.miami.edu/forecasts/n34plume.static.today.html) Nino 3.4 plume
- [Global Mean Surface Temperature Plume](https://nmme.earth.miami.edu/forecasts/gmt_plume.today.html)
- [Global probability maps](https://nmme.earth.miami.edu/forecasts/nmme_prob_forecast_all_var.html) of temperature, precipitation, and SSTs
- [Global anomaly maps](https://nmme.earth.miami.edu/forecasts/nmme_forecast_all_var.html) of temperature, precipitation, and SSTs (<i>with updated 1991-2020 climatologies</i>)
<h2></h2>
[This menu is hot off the press, so bare with us, especially on mobile, as we fine tune.](https://nmme.earth.miami.edu/forecasts/index.html) Buon appetito! 
<br><br>

<div style="text-align: right"><i> - :pinched_fingers: :pinched_fingers: :pinched_fingers: <a href="https://seasonedchaos.github.io/people/kayla-besong/">Kayla Besong</a></i></div>
<div style="text-align: right"><i> Graphics credit to: <a href="https://seasonedchaos.github.io/people/kayla-besong/">Kayla Besong</a> (thumbnail and figures)</i></div>


