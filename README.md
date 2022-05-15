<p style="font-size:34px; color:#051367">

# Toxic User Detection Using Social Network Analysis: Based on Dota2 Game Chat log
</b></p>

## Project Presentation
My presentation and portfolio for the final capstone can be found in the website below.

🖥 http://www.lee01key.com

## Problem Statement
<blockquote>
Milgram(1967) asserted that we all are connected to any other person on the planet, within six degrees of separation. A small world in a real life setting, MOBA (multiplayer online battle arena game), we can build a similar network of abusive language. In this case, this small tiny world can be problemtic and toxic. Utilizing Social Network Theory, I intend to find an effective way to detect and penalty toxic users.
</blockquote>
<br><br>


## 📈 Methods and processes
### &ensp;&ensp; Data
<blockquote>
I used an open-source dataset (<a href = "https://www.kaggle.com/datasets/devinanzelmo/dota-2-matches?select=chat.csv">link</a>). This dataset included 50,000 ranked ladder matches on a same day, from the DotA2 data dump created by OpenDota.

This dataset includes:
<li> 50,000 matches </li>
<li> 179,992 players </li>
<li> 1,439,488 chat logs </li>

</blockquote>
<br>


### &ensp;&ensp; EDA
<blockquote>
I checked profanity in chat using <code>ProfanityCheck</code> library.

Initial Findings:
<li> 7.09% of the chat included abusive language. </li>
<li> 59.95% of the match included abusive language. </li>
<li> 24.43% of the players spoke 100% of the abusive language. </li>
<li>85.19% of the players who listen to the abusive language spoke abusive language after the match. </li>
</blockquote>

<br>

### &ensp;&ensp; Social Network Analysis: Modeling
<blockquote>
I used <code> NetworkX </code> library to see the network structure of social networks of abusive langauge. Gephi was used for further visualization and network analysis.

<img src ="https://static.wixstatic.com/media/09ea23_a20715b29407439cb195681d32db5add~mv2.png/v1/fill/w_792,h_574,al_c,q_90,usm_0.66_1.00_0.01,enc_auto/Screen%20Shot%202022-05-12%20at%2010_46_47%20AM.png">
</blockquote>
<br>


### &ensp;&ensp; Results and Conclusions
<blockquote>
Findings suggest that imposing penalty on toxic user with high centrality and high betweenness centrality is effective for preventing abusive language dissemination
</blockquote>

<br></br>

## 🗂 File Structure of Project 3

#### &ensp;&ensp;📁 notebooks
##### &ensp;&ensp;&ensp;&ensp; 📑 1_data_cleaning_eda.ipynb
##### &ensp;&ensp;&ensp;&ensp; 📑 2_data_preprocessing.ipynb
##### &ensp;&ensp;&ensp;&ensp; 📑 3_social_network_analysis.ipynb
<br>

 #### &ensp;&ensp;📁 data
 
##### &ensp;&ensp;&ensp;&ensp; 📗 chat_original.csv
##### &ensp;&ensp;&ensp;&ensp; 📗 chat_preprocessed.csv
##### &ensp;&ensp;&ensp;&ensp; 📗 chat_sna_shaped.csv
##### &ensp;&ensp;&ensp;&ensp; 📗 wo_high_between.csv
##### &ensp;&ensp;&ensp;&ensp; 📗 wo_high_centrality.csv
##### &ensp;&ensp;&ensp;&ensp; 📗 wo_maluser.csv
##### &ensp;&ensp;&ensp;&ensp; 📗 wo_randuser.csv
##### &ensp;&ensp;&ensp;&ensp; 📗 wo_randuser1.csv

<br>

 #### &ensp;&ensp;📁 network_analysis
##### &ensp;&ensp;&ensp;&ensp; 📑 final_presentation (html and json files for portfolio webpage)

##### &ensp;&ensp;&ensp;&ensp; 🎥 time_interactive_social_network.mov


<br><br>

## References
<font face = "georgia">

Donghyun Ahn, Hwigang Kim. (2018). A method to detect malicious users with high influence through the analysis of profanity networks in MOBA games.  Journal of the Information Science Society , 45(12), 1312-1318.


C. Gao, J. Liu, and N. Zhong, Network immunization and virus propagation in email networks: experimental evaluation and analysis, Knowledge and information systems, Vol. 27, No. 2, pp. 253-279, 2011.


E. Bakshy, I. Rosenn, C. Marlow, and L. Adamic, The role of social networks in information diffusion, Proc. of the 21st international conference on World Wide Web, pp. 519-528, 2012.