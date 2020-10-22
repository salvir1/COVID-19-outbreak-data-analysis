# COVID-19 trend analysis. Is it an outbreak or an uptick?

<img align="right" src="img/COVID-cases-by-outbreak-groupings.png" width='500' height='auto' ></img>

## Overview
This repo is an ongoing project to explore the geographic patterns over time in the COVID-19 pandemic. The goal is to identify meaningful observations that could potentially be used by entities that are seeking to control and/or respond to the crisis.

This is an ongoing project. New information will be added soon. Please recognize that the ideas and reasearch in this repo are a work in process.

## Goals

The goals of this project are:
> - To look for meaningful patterns in the geogrpahic progression over time of the COVID-19 pandemic
> - To work with various EDA and data visualization tools and techniques

## Tools and techniques used in this project
- **Tools**
> - Python, Jupyter Lab, SciKitLearn, Pandas, Numpy
- **Visualization**
> - Plotly, Matplotlib
- **Techniques**
> - Supervised learning model development, spatial mapping, simple moving average

## COVID-19 trend analysis

### Data and EDA
Data for the COVID-19 trend analysis was obtained from the following source:
- [the COVID Tracking Project](https://www.covidtrackingproject.com), Creative Commons CC BY 4.0 license

For the US data, state groupings were created for outbreaks of similar scale and timeframe. States were grouped into one of four categories: spring outbreak, summer outbreak, fall outbreak, and no outbreak. Information about these groupings can be found later in the repo.

Case and death data was smoothed using a 14 day simple moving average since the daily reports are quite noisy.

### Findings and comments

<img align="center" src="img/COVID-cases-by-outbreak-groupings.png" width='1000' height='auto' ></img>

This chart reveals a number of interesting patterns.

> - While the *spring outbreak* was occurring, the infection rate was surprisingly uniform among the other groups.
> - The *summer outbreak* emerged quickly. The *fall outbreak* group and *no outbreak* group maintained comparable infection rates even as the the rates crept up (perhaps due to states easing restrictions en masse). The reported infection rate for the *summer outbreak* group suprassed that of the *spring outbreak*. This could be explained in part by increased testing.
> - The *fall outbreak* ramped up quickly as well. It appears to be headed towards a higher peak than either of the two previous outbreaks. Fortunately, this outbreak is affecting a much smaller portion of the US population than the previous two at this time.
> - The rapid ramp-ups of the summer and fall outbreaks suggest an early warning system may be necessary to *see* an emerging outbreak before its too late. By the time the trends start to change in the case rate data it may be too late to avoid an outbreak. 

<img align="center" src="img/COVID-deaths-by-outbreak-groupings.png" width='1000' height='auto' ></img>

Deaths are the most important measure of severity of the outbreak.

> - The impact of the outbreaks are clearly visible in the charts. The shaded area in the chart above represents the cost in terms of lives lost from the summer outbreak. This outbreak led to an additional 23,000 lives lost as compared to baseline. 
> - Governments and public health agencies are unlikely to drive the death rate down to zero until a vaccine is available, but they can work to avoid an outbreak to avoid the associated costs of lives lost.
> - *Deaths per 100,000* was much smaller for the second outbreak than the first.
> - It's too early to say what the death rate will look like for the third outbreak. Recent news reports--which are not yet reflected in the data--suggest the death rate may end up being worse. Over the past several days, the Dakotas reported death rates exceeding 0.5 people per 100,000.

<img align="center" src="img/COVID-case-fatality-by-outbreak-groupings.png" width='1000' height='auto' ></img>

Note that the reported death time series was shifted forward by 14 days to synchronize up better with the case time series so that an accurate case fatality ratio could be calculated.
What are the takeaways from this chart?

> - The case fatality ratio has been reduced significantly from the early days of the pandemic. This can probably be attributed to several factors. For one, much more testing is being done, so fewer cases are being missed. For two, the medical community knows much more about how to care for patients with the disease, which has probably led to better outcomes. 
> - The case fatality ratio crept up a bit for the summer outbreak group, but otherwise hasn't seen marked changes after spring ended. There's no strong indication that summer's crowded hospitals had a major impact on case fatality--at least in this slice of the data.

### State groupings

Spring outbreak
- Occurred primarily in the northeast, Michigan, and Louisiana
- Exceeded 40 cases per 100,000 per day or 0.8 deaths per 100,000 per day before May
- About 80M people are in this group
Summer outbreak
- Occurred primarily in the southeast and Arizona
- Exceeded 40 cases per 100,000 per day or 0.5 deaths per 100,000 per day between June and August
- About 80M people are in this group
Fall outbreak
- Upper midwest and Arkansas at this time with more states to be added if they meet the threshholds
- Exceeded 40 cases per 100,000 per day or 0.5 deaths per 100,000 per day after August
- About 11M people are in this group
No outbreak
- Avoided classification in one of the other outbreak categories
- About 160M people are in this group

### Areas for further study

- Describe and then model an *early warning system* that could identify when the infection rate for a region such as a state is threatening to become an outbreak.
- Analyze data from other regions of the world that have seen outbreaks with similar timing such as Europe.

## Contributors
[Rob Salvino](https://github.com/salvir1)


## License
[MIT ©](https://choosealicense.com/licenses/mit/)
