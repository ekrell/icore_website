# iCORE Newsletter – 2023/10/24

![logo](../img/logo_plain_sm.jpg)

The iCORE newsletter highlights events and information related to the [innovation in COmputing REsearch (iCORE) lab](https://icore.tamucc.edu/),
as well as the broader GSCS/CS programs at Texas A&M University - Corpus Christi and whatever else might interest that community.
If you have any news or resources you would like to share, send an email to [Evan Krell](https://scholar.google.com/citations?user=jLuwYGAAAAAJ&hl=en) (ekrell@islander.tamucc.edu).

[See past newsletters.](https://github.com/ekrell/icore_website/tree/main/news)

## Welcome

![Sunset on Padre Island](../img/beachday_sunset.jpg)

A beautiful sunset at the beach on Padre Island. It is mid-October and the water temperature is still very pleasant for a swim. 

Welcome to another iCORE Newsletter. 

## iCORE Meetings

**[iCORE Teams meeting link](https://teams.microsoft.com/l/meetup-join/19%3Ameeting_MDdlZDBiMTgtYzVjNS00YjhhLWE5OTctY2Y5YzMyYTljNzU5%40thread.v2/0?context=%7B%22Tid%22%3A%2234cbfaf1-67a6-4781-a9ca-514eb2550b66%22%2C%22Oid%22%3A%22994c008b-0707-4f3c-8ac0-73b65e733430%22%2C%22MessageId%22%3A%220%22%7D)**

### Fall 2023 iCORE Event Calendar

![Event calendar](../img/icore_events_fall2023.png)

### Previous Meeting: October 20, 3:30 - 5:00 PM

In the last meeting, Evan Krell presented an introduction to using [Inkscape](https://inkscape.org/) to create high-quality vector research graphics for publication. Inkscape is an open source software for designing vector graphics; a free alternative to Adobe Illustrator. the iCORE event calendar above was designed in Inkscape. He discussed the advantages of vector graphics of rasters and showed how to use the basic tools to create diagrams and add elements to a map. He also showed that the output of Python's `matplotlib` can be modified in Inkscape if they have been saved as PDFs. Each plot element is maintained as an independent object so it's easy to make modifications without loss of quality. 

Unfortunately, there were several timing conflicts and it is no wonder that most chose to attend [Donna Shaver](https://www.gulfbase.org/people/dr-donna-j-shaver)'s sea turtle talk hosted by our friends of the [Marine Science Graduate Student Organization](https://msgsoresearchforum.wixsite.com/msgsosymposium). There was a very small crowd in iCORE last Friday, but I will share the recording in the future.

### Next Meeting: November 3, 3:30 - 5:00 PM

- **3:30 - 4:00 PM:** General updates
- **4:00 - 5:00 PM:** Unit Testing lecture by Tami King

## Upcoming Events

Friday, November 3rd is going to be a very busy day: Xiaojun Qiao and Evan Krell are both defending. Xiaojun is defending his PhD dissertation and Evan is presenting his proposal. Both are students in the Geospatial Computer Science PhD program. The contents of the snacks at their seminars are still to be determined. I know most of you only show up for the free food. These are followed by a programming lecture in iCORE, presented by Tami King. 

### GSCS Dissertation Defense: Xiaojun Qiao

- **Speaker:** Xiaojun Qiao
- **Subject:** Assessment of Land Subsidence Along the Texas Gulf Coast
- **Date:** Friday, November 3, 2023
- **Time:** 9:00 a.m.
- **Committee:** Dr. Philippe Tissot; Dr. Scott King; Dr. Feiqin Xie; Dr. Mohan Rao (Graduate Faculty Representative)
- **Location:** Center for Instruction (CI) 128
- **Zoom:** https://tamucc.zoom.us/j/98145116858?pwd=eDNoSUN2NEhrL3FYRkVTRlN4eGNnZz09 

**ABSTRACT:**

The Texas Gulf Coast has been recognized as one of the subsidence hotspots in the United States, thereby presenting risks such as shoreline erosion and coastal flooding. The accurate estimation of subsidence and the identification of its underlying causes hold significant value for comprehending subsidence processes and guiding decision-making. To achieve this, the research integrated space-borne and terrestrial geodetic techniques, utilized multi-source observations, and applied machine learning (ML) methods for the estimation, modeling, and attribution of subsidence along the Texas Gulf Coast. First, two sea-level difference methods were designed to reconstruct displacement time series at tide gauge (TG) locations in Texas with observation periods exceeding ten years. In addition, synthetic aperture radar (SAR) imagery, continuously operating global navigation satellite system (cGNSS) observations, and sea-level measurements were harnessed to estimate the spatio-temporal patterns of subsidence spanning around three decades since the 1990s at the Eagle Point TG station, a prominent hotspot of sea-level rise in the United States. Moreover, the interferometric SAR (InSAR) was leveraged to generate a large-scale subsidence map along the Texas coastlines post-2016. Attribution analysis indicated that hydrocarbon extraction and groundwater withdrawal were the predominant factors responsible for identified subsidence hotspots in the Texas Gulf Coast. ML demonstrated an impressive performance (with an R2 of 0.56) in modeling the observed large-scale subsidence, by incorporating a range of features related to natural terrain variations and anthropogenic activities. Explainable artificial intelligence (XAI) methods provided quantitative estimates of feature contributions of the ML model, and the data-driven results revealed that the digital elevation model (DEM) and anthropogenic factors were contributing features in relation to subsidence.


### GSCS Proposal Defense: Evan Krell

- **Speaker:** Evan Krell
- **Subject:** Clustering Strategies For Explainable AI (XAI) with Correlated, High-Dimensional Geoscience AI Models
- **Date:** Friday, November 3, 2023
- **Time:** Noon
- **Committee:** Dr. Scott King; Dr. Philippe Tissot; Dr, Antonio Medrano; Dr. Imme Ebert-Uphoff; Dr. Antonios Mamalakis
- **Location:** To be determined
- **Zoom:** To be determined

**Abstract** 

With the rapid deployment of high-resolution sensors and models, geospatial data is captured and generated at an extremely high rate. By automatically extracting information from large data volumes, machine learning is increasingly used to turn massive geospatial data into geoscience insights. There is widespread use of high-dimensional raster data from which complex machine learning algorithms learn to recognize spatial and spatial-temporal patterns. These models may be used for critical decision-making or as a way to aid scientific discovery. Complex models can learn high non-linear relationships to achieve high performance, but there is a concern that their complexity makes it very difficult for users to determine how the model reached its decision. This has motivated the widespread adoption of explainable artificial intelligence (XAI) techniques that probe the model in various ways to explain how it works. XAI methods are highly sensitive to correlations among input predictors. Proposed mitigations involve grouping correlated predictors and applying XAI to groups instead of individuals. However, there are major challenges to grouping the grid cells of geoscience rasters based on their correlation. These datasets are commonly high-dimensional with substantial autocorrelation. Conventional techniques for grouping correlated tabular features are rarely applicable. The purpose of this research is to develop strategies for using data-driven clustering techniques to group raster data to improve the accuracy of XAI results. First, we describe the limitations of current approaches and identify XAI challenges related to raster-based geoscience models. We then develop a set of benchmarks so that we can quantitatively assess XAI methods in a variety of complex scenarios. Finally, we propose and evaluate methodologies for applying clustering and XAI techniques. These include a hierarchical clustering approach to automatically investigate multiple scales of patterns in high-dimensional data. 

### Programming Tutorial: Unit Testing

- Speaker: [Tami King](http://web.cse.ohio-state.edu/~king.281/) 
- When: Friday, Nov. 3, 4:00 - 5:00 PM
- Where: iCORE (NRC 2100 suite)

Tami King will present a lecture on unit testing. This refers to a software development process where the code is developed in small modules and thoroughly tested in isolation. The larger software product is composed of these well-understood components called units. There are many advantages to using unit testing to drive software development, as Mrs. King will discuss. 

Tami King works remotely, from Corpus Christi, for the Computer Science and Engineering Department at Ohio State University. If you haven't figured it out yet, she is the wife of iCORE's own Dr. King and we are all in trouble if her talk is not well-attended. 

## Upcoming Conferences

### AGU Annual Meeting 2023 (San Francisco, CA)

| **Speaker** | **When**               | **Topic**                                                                                                                                                                     | 
|-------------|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Wen Zhong   | Dec. 12, 18:24 - 18:27 | The Impact of Potential Land Subsidence on a Future DEM Based on InSAR, Airborne LiDAR, and Deep Learning                                                                     | 
| Marina Vicens-Miquel | Dec. 15, 16:10 - 20:30 | Advancing Coastal Inundation Frequency Predictions with an AI-based Sub-seasonal to Multi-year Water Level Model in the Gulf of Mexico                                        | 
| Evan Krell  | Dec. 15, 10:30 - 14:50 | Exploring the Influence of Correlated Features on Geoscience AI Models to Improve the Scientific Insights Gained From Using Explainable AI Techniques for Feature Attribution | 

(Would it be improper to point out that I submitted an abstract to AGU because I wanted to eat cioppino and dim sum in SF?)

## Get involved

As always, we encourage all iCORE members and iCORE-adjacent persons to get involved and propose workshop/lecture/training ideas that they would like to present.

## iCORE resources

- location: NRC 2100 Suite (https://goo.gl/maps/Htbp1YMASAmYqkFu9)
- website: http://icore.tamucc.edu/
- twitter: https://twitter.com/ICORE_TAMUCC
- youtube: https://www.youtube.com/channel/UCvsK07PvushTI2BA2BhN-DQ
- discord: https://discord.gg/3eeMN229cr





