=MEDIAN(

IF(

&nbsp;   (jobs\[job\_title\_short]=A2)\*

&nbsp;   (jobs\[job\_country]=country)\*

&nbsp;   (ISNUMBER(SEARCH(type,jobs\[job\_schedule\_type])))\*

&nbsp;   (jobs\[salary\_year\_avg]<>0),

&nbsp;   jobs\[salary\_year\_avg]

)

)

