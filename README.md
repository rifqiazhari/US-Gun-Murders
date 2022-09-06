# US-Gun-Murders
![alt text](a55b3c9d-cdc7-45a6-8604-f9864a9f1c39.png)
# Code
`r <- murders %>%`<br/>
&emsp;&emsp;`summarize(rate = sum(total) / sum(population) * 10^6) %>%`<br/>
&emsp;&emsp;`.$rate`<br/>
    
`murders %>%`<br/>
&emsp;&emsp;`ggplot(aes(population/10^6, total, label = abb)) +`<br/>
&emsp;&emsp;`geom_abline(intercept = log10(r), lty = 2, color = "darkgrey") +`<br/>
&emsp;&emsp;`geom_point(aes(col = region), size = 3) +`<br/>
&emsp;&emsp;`geom_text_repel() +`<br/>
&emsp;&emsp;`scale_x_log10() +`<br/>
&emsp;&emsp;`scale_y_log10() +`<br/>
&emsp;&emsp;`xlab("Population in millions (log scale)") +`<br/>
&emsp;&emsp;`ylab("Total number of murders (log scale)") +`<br/>
&emsp;&emsp;`ggtitle("US Gun Murders in 2010") +`<br/>
&emsp;&emsp;`scale_color_discrete(name = "Region") +`<br/>
&emsp;&emsp;`theme_economist()`<br/>
