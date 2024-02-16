---
layout: post
title: Weather Regimes&#58; The Atmosphere&#39;s Preferred Moods
description: During the course of a day, your mood might change several times – from the simple joy instilled by a great cup of coffee, to a transient flash of road rage.
tags: [weather, climate, subseasonal, predictability]
comments: true
category: blog
Date: 02/16/2024
img: mood-cluster_thumbnail.png
authors: Simon Lee
---

<div style="text-align: center">Simon Lee</div>
<br>
<i>Bio: [Simon Lee](https://simonleewx.com/) is currently a Postdoctoral Research Scientist in the Department of [Applied Physics and Applied Mathematics](https://www.apam.columbia.edu/) at Columbia University, working on large-scale extratropical weather and climate variability and predictability. He’s moving to the [University of St Andrews](https://www.st-andrews.ac.uk/earth-sciences/) (Scotland) in July, as a Lecturer (Assistant Professor) in Atmospheric Science.</i>
<br><br>

During the course of a day, your mood might change several times – from the simple joy instilled by a great cup of coffee, to a transient flash of road rage. But over the course of several days to a week, one overall mood might characterise how you feel – perhaps you’re particularly satisfied with your job, or maybe you’re on vacation and feeling relaxed. Well, it turns out, the atmospheric flow also has such [slowly-varying](https://seasonedchaos.github.io/What-Can-the-Tropics-Tell-Us-About-Next-Weeks-Weather/) “moods”. These atmospheric moods are called [<i>weather regimes</i>](https://doi.org/10.1175/1520-0469(1995)052<1237:WRRAQS>2.0.CO;2).
<br><br>
The idea behind weather regimes is that we can classify the atmospheric flow larger than individual weather systems into clusters, called regimes. You can think of it a bit like collections of moods that fall under the same umbrella. These regimes are <i>recurrent</i> (they happen repeatedly), <i>persistent</i> (they last for multiple days), and <i>quasi-stationary</i> (the pattern stays in the same place). 
<br>
<h2>Classifying the atmosphere’s moods</h2>

By the mid-20th century, [meteorologists in the UK](https://doi.org/10.1002/j.1477-8696.1949.tb05487.x) had noted that certain types of weather seemed to persist longer than the individual weather systems themselves. These weather types were classified subjectively by manually inspecting weather charts (hard to fathom nowadays!). 
<br><br>
As the 20th century progressed, a lot of work went into [<i>teleconnections</i>](https://www.climate.gov/news-features/blogs/enso/what-are-teleconnections-connecting-earths-climate-patterns-global) – the idea that atmospheric circulation anomalies at one location are correlated with those far away. Some of these include the [North Atlantic Oscillation](https://seasonedchaos.github.io/Seasoned-Chaos-presents-the-North-Atlantic-Oscillation/) (NAO) [no, not the [Scottish band](https://soundcloud.com/northatlanticoscillation)] and the [Pacific-North American pattern](https://seasonedchaos.github.io/Teleconnection-Telenovela-Pasion-of-the-Pacific-North-American-Pattern/).
<br><br>
Although teleconnections and regimes aren’t entirely unique concepts, teleconnections can only tell you about one part of the atmospheric flow at once. If you asked the atmosphere, “<i>how are you feeling today?</i>”, it could respond by telling you, “<i>well, I’m feeling strongly PNA+ but slightly NAO-...</i>” (and a whole host of [other indices](https://www.cpc.ncep.noaa.gov/data/teledoc/telecontents.shtml)… let’s not worry about them). You would then have to work out what that combination meant for you (is the atmosphere actually in a good mood?). Alternatively, the atmosphere could have simply told you what the regime is: “<i>I’m feeling Pacific Trough-y today</i>”.
<br><br>
Looking under the hood, defining regimes usually involves some sort of clustering [algorithm](https://www.youtube.com/watch?v=X8f5RgwY8CI). The most commonly used is called <i>k</i>-means clustering. To use it, you give the algorithm the data you’re interested in organising, and tell the algorithm how many clusters (moods) you’d like. It then solves for the “centroids” (the centres of each cluster). In essence, each data point is assigned to a cluster, and the (squared) distance from the centre of that cluster is computed. By repeatedly trying different centroids, the algorithm eventually finds the centroids that minimise the sum of these (squared) distances.  When finding weather regimes, 500 hPa geopotential height anomalies (i.e., mid-level pressure patterns) are usually used, since this field represents the large-scale variability in the troposphere well (and generally doesn’t run into any mountains). 
<br><br><br>
<center><img src="/assets/img/kmeans-cluster.gif" width="70%"></center>
<br><sub><i>Convergence of k-means clustering into three clusters. (Source: <a href="https://commons.wikimedia.org/wiki/File:K-means_convergence.gif">Wikimedia Commons</a>)</i></sub>
<br><br>
Returning to the mood analogy, you can imagine this clustering procedure as being like grouping together all your specific moods into overarching mood states – for example, one cluster could contain all ‘sad’ moods, incorporating more specific feelings such as anxious, lonely, or frustrated (representing individual weather systems).
<br><br>
<img src="/assets/img/mood-cluster.png" width="99%">
<br><sub><i>An example of how we can cluster moods into (left) two or (right) four mood 'regimes' – indicated by color shade – based on where the mood lies on philosophical axes of feeling (negative to positive) and energy (low to high).</i></sub>
<br><br>
<h2>The New Mood (year-round!)</h2>

Mid-latitude dynamicists have historically tended to focus on winter, because the variability is a bit more ✨ dramatic ✨, and phenomena like [ENSO](https://seasonedchaos.github.io/Round-1-ENSO-is-King/) and the [polar vortex](https://seasonedchaos.github.io/Things-are-getting-heated-the-science-behind-the-polar-vortex-and-stratospheric-warmings/) are active and kicking the atmosphere into certain patterns. There’s already been a lot of work on wintertime weather regimes dating back to the 1980s. But, thankfully, winter is just one season! So how do we define regimes year-round? In a [recent paper](https://doi.org/10.1175/JCLI-D-23-0214.1), we do just that and classify year-round regimes over North America. Let’s dig into some of the maths-y details… 
<br><br>
Before attempting year-round regimes, we need to deal with the fact that there’s more atmospheric variability in the winter than the summer. This is important because we’re using a clustering algorithm that deals with variance, which would otherwise overemphasise winter and de-emphasise summer. Not good!
<br><br>
To get around that, we normalise the anomalies: we divide by the North America-average grid-point standard deviation of the anomalies for each day of the year. That’s quite a wordy sentence, but in simple terms this procedure means that <i>k</i>-means can treat winter and summer equally.
<br><br>
Now that we’ve dealt with the variability problem, the big question is: <b>how many regimes?</b> In our study, we performed various different tests and found that four regimes clearly emerged as the best solution. So, the atmosphere  over North America has four ‘moods’! But what about those cases when the atmosphere isn’t in any particular mood – when the atmospheric flow isn’t anomalous? We reclassify these days as “No Regime”, and so we actually have five states:
<br><br>
<img src="/assets/img/year_round_american_regimes_1979_2022_5panel.png" width="95%">
<br><sub><i>Average 500 hPa geopotential height anomalies during (a–d) four year-round North American weather regimes and (e) No Regime. The percent of days assigned to each regime are shown in brackets.</i></sub>
<br><br>
The <i>Pacific Trough</i> regime is known for supplying the [West Coast](https://www.youtube.com/watch?v=QBPE2fZsVYU) with drenching atmospheric rivers, and is more common during El Niño. The <i>Pacific Ridge</i> regime is a bit of a chaotic player and often brings big temperature contrasts across North America – it is the coldest regime in the west and the warmest in the east – and is more common during La Niña. <i>Alaskan Ridge</i> likes to grab the headlines with [cold air outbreaks](https://seasonedchaos.github.io/The-Enchanting-Tale-of-Cold-Air-Outbreaks/), which it often brings to the eastern US and Canada, and drought in California. Meanwhile, <i>Greenland High</i> – which is similar to the negative NAO – is the one that East Coast snow lovers lust after, and is more common when the polar vortex is weak.
<br><br>
<h2>So what’s the point?</h2>

Interest in regimes has burgeoned alongside interest in subseasonal-to-seasonal (S2S) prediction. Regimes naturally sit somewhere between weather and climate, and so they can serve as one tool to ‘bridge the gap’ between the two. Previous studies have utilised regimes in understanding [windows of opportunity](https://doi.org/10.1175/BAMS-D-18-0326.1) for extended-range prediction and in diagnosing ‘[flow-dependent predictability](https://doi.org/10.1002/qj.3265)’, where forecast skill depends on the state of the atmosphere.
<br><br>
More generally, regimes serve as a simple and objective method for quickly interpreting the “big picture” from increasingly large ensembles, such as the 101-member, daily, 46-day forecasts from [ECMWF](https://charts.ecmwf.int/products/extended-regime-probabilities?forecast_from=latest). Using regimes means it only takes a forecaster a few minutes to gauge the mood of the atmosphere (present and future) in such large amounts of data. Take this example below, from the GEFS: Alaskan Ridge transitions into No Regime within the first week of the forecast, before a likely transition into Pacific Ridge by the end of February. Things then look more uncertain going into March, but the probability of Greenland High is above-normal while all other regimes are below-normal.
<br><br>
Is this a window of opportunity? Now that puts me in a good mood.
<br><br>
<img src="/assets/img/regimes_gefs_20240215.png" width="90%">
<br><sub><i>Global Ensemble Forecast System (GEFS) North American weather regimes, initialised on 15 February 2023. [https://simonleewx.com/gefs_north_america_regimes/](https://simonleewx.com/gefs_north_america_regimes/) </i></sub>
<br><br>


<br><br>
<div style="text-align: right"> <i>Written by: <a href="https://simonleewx.com/">Simon Lee</a></i> </div>
<div style="text-align: right"> <i>Graphics credit to: Wikimedia Commons (clustering animation), <a href="https://seasonedchaos.github.io/people/kayla-besong/">Kayla Besong</a> (thumbnail, mood cluster diagram), and <a href="https://simonleewx.com/">Simon Lee</a> (year-round North American weather regimes, GEFS North American weather regime forecast)</i></div>




