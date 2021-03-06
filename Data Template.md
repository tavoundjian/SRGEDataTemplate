Title: SRGE Dataset Template
Date: 2016-11-08 08:00
Tags: SRGE
Category: SRGE
Slug: srge-data-template
Summary: Guidelines for setting up your reactor data 

Hello, this is an example of some text.

#SRGE Dataset<sup>1</sup> Template
|Variable|Required or Optional|Description|Example Values|Comments/Other Requirements|
|---|---|---|---|---|			
|Case Status|Required|Binary identifier of early syphilis cases|<ul><li>1 = Presence of Disposition Code for Primary, Secondary or Early Syphilis (710, 720, 730)</li><li>0 = Otherwise</li></ul>|Case status must be a binary variable <br> Case definition may be modified based on health department needs and/or priorities|
|Age Group|Required|Categorical variable indicating age|<ul><li>11-19</li><li>20-24</li><li>25-29</li><li>30-34</li><li>35-39</li><li>40-44</li><li>45-49</li><li>50-54</li><li>60-64</li><li>65-69</li><li>70+</li></ul>|Cut-points and age range are flexible and can be defined based on age distribution of population of interest|
|Titer Value|Required|Categorical variable indicating titer result from RPR or VDRL test|<ul><li>Non-R</li><li>1:1</li><li>1:2</li><li>1:4</li><li>1:8</li><li>1:16</li><li>1:32+</li></ul>|Qualitative titer values can be included or excluded from reactor grid. SRGE does not provide support for cleaning or grouping qualitative results|
|Gender|Optional|Categorical variable indicating gender|<ul><li>Male</li><li>Female</li></ul>|If data is available on lab report, gender can be used to reflect sexual preference or non-binary gender|
|Test Type|Optional|Categorical variable indicating type of non-treponemal test performed|<ul><li>RPR</li><li>VDRL</li></ul>|All lab reports should correspond to non-treponemal tests only.<br>Blood false positives (i.e., negative treponemal test, but reactive non-treponemal test) should be accounted prior to importing data into SRGE|				
|Previous Result|Optional|Categorical variable indicating change in titer from previous result|1 = Less than 2 titer increase<br>0 = New positive or 2+ titer increase|Comparison to previous result must be performed prior to importing data into SRGE.<br>Example SAS code for comparing results is available here:|
<sup>1</sup>Data set requirements: Data set should be in a .txt or .csv format and include all lab reports for non-treponemal tests (RPR and/or VDRL labs) from the specified time period. Blood false positives (i.e., reactive non-treponemal tests with a negative treponemal test) should be excluded prior to importing data into SRGE. 