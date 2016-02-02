# Diabetes
A brief analysis of the AIM94 diabetes dataset

The dataset analyzed here was collected for the 1994 AI in Medicine Symposium and is hosted at the UCI Irvine Machine Learning Repository.  The dataset contains blood glucose and other measurements for 70 patients with Insulin Dependent Diabetes Mellitus (IDDM).  The following excerpt explains the data codes in this set:

"Diabetes patient records were obtained from two sources:  an automatic electronic recording device and paper records.  The automatic device had an internal clock to timestamp events, whereas the paper records only provided "logical time" slots (breakfast, lunch, dinner, bedtime).  For paper records, fixed times were assigned to breakfast (08:00), lunch (12:00), dinner (18:00), and bedtime (22:00).  Thus paper records have fictitious uniform recording times whereas electronic records have more realistic time stamps.

Diabetes files consist of four fields per record.  Each field is separated by a tab and each record is separated by a newline.

File Names and format:  
(1) Date in MM-DD-YYYY format  
(2) Time in XX:YY format  
(3) Code  
(4) Value"  

So what we are dealing with here is time series data with somewhat fictitious uniform time stamps for part of the data set.  

The following excerpt is from the domain description provided for the symposium:

"Patients with IDDM are insulin deficient. This can either be due to a) low or absent production of insulin by the beta islet cells of the pancreas subsequent to an auto-immune attack or b) insulin-resistance, typically associated with older age and obesity, which leads to a relative insulin-deficiency even though the insulin levels might be normal.

Regardless of cause, the lack of adequate insulin effect has multiple metabolic effects. However, once a patient is diagnosed and is receiving regularly scheduled exogenous (externally administered) insulin, the principal metabolic effect of concern is the potential for hyperglycemia (high blood glucose). Chronic hyperglycemia over a period of several years puts a patient at risk for several kinds of micro and macrovascular problems (e.g. retinopathy). Consequently, the goal of therapy for IDDM is to bring the average blood glucose as close to the normal range as possible. As explained below, current therapy makes this goal a very challenging (and often frustrating) one for
most patients. One important consideration is that due to the inevitable variation of blood glucose (BG) around the mean, a lower mean will result in a higher frequency of unpleasant and sometimes dangerous low BG levels."

To summarize in layman's terms, both high and low blood glucose levels are very unhealthy for the diabetes patient.  

My objective in analyzing this dataset is to see if I can fit a simple linear model that will look for secular (consistently increasing or decreasing) trendds in the time series data.  A secular trend in the wrong direction would indicate that the patient needs attention.
