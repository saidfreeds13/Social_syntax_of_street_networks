# Former industrial neighborhoods of St. Petersburg: assessing relationship between street-network morphology and social organization of space. 
*Developed by Bereiya Said, 2nd year master student of IDU ITMO*
## Introduction ##
More often than not former industrial districts of USA and Europe experience the consequences of being "left-behind". "Left-behindness" entails a variety of socio-spatial externalities such as physical deterioration of infrastructure, an increased social tension among its residents, stigmatization of space. These are what an American geographer Ed Soja called "metropolarities", giving rise to all kinds of social and spatial paradoxes. To initiate a more evidence-based regeneration projects and policy for these areas, a deep understanding of the exisitng space-society relationships is required. It is in the scope of this thesis to identify and characterise the forms of (paradoxical) relationships between the morphological configuration and social organization of space in the former industrial areas. The street-network, and a street as its element, is taken as an object, allowing for porous movement between a micro-level and a meso-level scale of an analysis. The city of interest is St. Petersburg (Russia) which has an immense territory of previous industrial use now referred to as "Gray Belt". The theoretical foundation is the research movement dubbed "Spatial Cultures," which emerged under the influence of Émile Durkheim’s sociology and the Space Syntax theory of Hillier and Hanson.

A. The Block-Scheme of the method 
B. [The method's explanation](https://github.com/saidfreeds13/Theiss_package/tree/master?tab=readme-ov-file#b-the-methods-explanation) 
C. Installation
D. Experimental application


## A. The Block-Scheme of the method ##
Street-network morphology via Space Syntax is taken for the  and its key measures of Integration and Choice. Whereas, the social organization is uderstood as a pattern of streets' functionality across the neighborhood. The operationalization for the social organization is done via a diveristy metric, showing how diverse and dense the functional uses of each street's segment.  

<p align="center">
  <img width="645" height="1002" alt="BS_methodology drawio" src="https://github.com/user-attachments/assets/3411a3d7-996a-4321-badd-f8f31f8f8af8">
</p>
<p align= "center"> *The block-scheme of the method, author: Bereiya Said 2nd year master student of IDU ITMO* </p>


## B. The method's explanation ## 
The main ETL-algorithms are packed in the library "streets_syntax_social" (installation instructions below)

### 1. A street-network dataset with syntactic and functional diversity metrics  ###
The key function of the method is "streets_social_sdataset".
``` 
streets_social_sdataset(
    uf = ,
    streets_m = ,
    package = "",
    save_file="",
    functions_subgroup_col_name = "",
    functions_subgroup_col_alias = "",
    urban_function_id = "",
    urban_function_type_name = "",
    morpho_metrics_list_cols = ["","", "", ""]
    )
```
Taking a street-network with morphological values and the urban functions (points), it builds a geo-dataset of street segmetns (LineString) with columns containing the syntactic and functional diversity metrics. Depending on the parameters set by a user, the number of characteristical columns may vary from four up to thirty. 

#### 1.1 Visualization ####
The results are then visualized with a function "visuals", essentially generating the choropleths of all metrics (both syntactic and functional). 
These maps can be compared between each other, especially those of morphology and functional diversity.    

#### 1.2 Interpretation ####
As a result, a user arrives at two distinct street hierarchies: the one of physcial dimension and the one of social dimension of a network. The distribution of syntactic values of all streets reveals the patterns of to-/through- movement logic, while the distribution of functional diversity metrics identifies socially appropriated of to-/through- movement logic. Obviously, these two hierarchies are bound to have mismatches; however, the nature and the intensity of the mismatches are dependent on the territorial assets and issues.  

### 2. Mismatches' identification ###
However, at this stage the relatiosnhips between these two hiararchies lack the direct systematic juxtoposition. The function "streets_mismatched" addresses the issue. 


The method may be adopted more broadly in the analysis of other cities and other type of districts. Yet, the initial hypotheses as to what type of relationships are more likely to take place in the area of study is a helpful prerequisite to the analysis and modeling. 


## Method installation ##
In order to install the package, containng the method use python environmnent such as Colab, Jupeter Notebooks. 

Firstly, clone the repo:
``` 
!git clone https://github.com/saidfreeds13/Theiss_package/
```
Then, install the git package and extract the package:
```
!pip install git+https://github.com/saidfreeds13/Theiss_package.git

!pip install theiss-package
```
Finally, import the method:
```
import streets_syntax_social 
```


## Experimental application ##

## Intermediate results ##
<p align="center">
  <img width="1010" height="2400" alt="BS_methodology drawio" src="s0.png">
</p>
---
