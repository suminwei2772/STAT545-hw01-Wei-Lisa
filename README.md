# STAT545

# Table of Contents
- [Introduction](#introduction)
- [Course Material](#course-material)

## Introduction   

Hi, My name is Lisa Wei. I am currently a graduate student in the UBC Bioinformatics Training Program. I am working in [Dr. Marco Marra's group](http://www.bcgsc.ca/faculty/mmarra) in the area of single cell genomics. 

Here are 2 cool tSNE plots showing 2-dimensional representations of transcriptome profiles of single cells. The graphs describe how similar each cell is to other cells that were profiled:

![alt text](https://itefe54628.i.lithium.com/t5/image/serverpage/image-id/95i99DF6E12B128CCAD/image-size/large?v=1.0&px=999)

Please view my [LinkedIn profile](https://ca.linkedin.com/in/lisa-wei-7806a373) for a more detailed description of my background and education during my undergrad.

I hope the STAT545/547 course will teach me more skills in programming in R and how to design good code.

## Course Material

Below are **links** to my reponses for weekly homework assignments:

* Homework 1 (Sept 19, 2017) 
   + [README.md for repo](README.md) - this current file you are reading
   + [README.md for hw01](/hw01/README.md)
   + [gapminder_hw01.md](/hw01/gapminder_hw01.md): Basic exploration of the gapminder dataset

* Homework 2 (Sept 26, 2017)
   + [README.md for hw02](/hw02/README.md) 
   + [Gapminder_dplyr_explore_hw02.md](/hw02/Gapminder_dplyr_explore_hw02.md): Using dplyr and ggplot2 to explore the gapminder dataset

* Homework 3 (October 3, 2017)
  + [README.md for hw03](/hw03/README.md)
  + [gapminder_dplyr_ggplot2_exploration.md](/hw03/gapminder_dplyr_ggplot2_exploration.md): Using dplyr and ggplot2 to explore specific aspects of gapminder including changes in life expectnacy over time and comparing distributions of GDP per capita between continents

* Homework 4 (October 10, 2017)
  + [README.md for hw04](/hw04/README.md)
  + [hw04_tidy_data_and_joints.md](/hw04/hw04_tidy_data_and_joins.md): Explores the Gapminder dataset with reshaping and various `join()` functions
  
* Homework 5 (October 17, 2017)
  + [README.md for hw05](/hw05/README.md)
  + [hw05_factor_figure_management.md](/hw05/hw05_factor_figure_management.md): Explores the singer dataset by performing factor re-leveling and re-ordering, modifying ggplot images, saving/reading in files/images
  
* Homework 6 (November 8, 2017)
  + [README.md for hw06](/hw06/README.md)
  + [hw06_data_wrangling.md](/hw06/hw06_data_wrangling.md): Explores writing functions and using `map()` to pull out certain subsets of a list, and using different operations to apply a function to a nested data frame.
 

* Homework 7 (November 14, 2017)
  + [README.md for hw07](/hw07/README.md)
  + [hw07_make.md](/hw07/hw07_make.md): is the final report which shows the distribution of word lengths and the number of words that start with each letter in the alphabet.
  
 
* Homework 8 (November 21, 2017)

	Created a Shiny app deployed here: https://suminwei.shinyapps.io/gapminder_shiny_app_on_git/
	+ [README.md for hw08](/hw08/README.md)
	+ [ui.R](/hw08/ui.R)
	+ [server.R](/hw08/server.R)
  
## Answers to questions posted for hw01 regarding providing a description of how this README.md file was written

- [x] Include a description of how you got the changes into README.md on GitHub.

I looked at the [R Markdown Cheatsheet](https://www.rstudio.com/wp-content/uploads/2015/02/rmarkdown-cheatsheet.pdf) to find out how to incorporate Markdown syntax into my file. Specifically, I included links, made certain words bold, put in section headers, and added bullet points. Also I referenced [Jenny Bryan's example README.md page as posted in the hw01 assignment](https://raw.githubusercontent.com/STAT545-UBC/STAT545-UBC.github.io/master/hw01_sample_readme.md).

* Links are made by putting square brackets around the word(s) you want the viewer to click on to go to the link, followed immediately by the website address in brackets.
* Section headers are made by putting one or more hash signs followed by the section header's name. There are different header levels. Level 1 headers has only 1 hash sign at the beginning, and with subsequent levels one adds on 1 extra hash sign every time.
* Bullets were put in by putting in a star * sign.
* Itallics were put in by putting 2 star signs ** on either side of the word.
* check-mark boxes were drawn by putting a dash and then square brackets around "x"

- [x] Did you edit in the browser at github.com?

I set up the repository and initiated the new repo with a REAME.md file on Github. I mostly edited in RStudio locally and then pushed the contents to Github. One mistake I made at first when I needed to delete a file was that I did it on Github rather than locally, after I've already cloned my repo to a local directory and was editing the files locally. I found this screws with the pushing and pulling. I tried to delete and rename files remotely and then pulling, but there were errors that came up. I also couldn't push any contents locally onto Github since the directory files were already changed on Github. So I ended up having to start a completely new project.

- [x] Did you pull, edit locally, save, commit, push to github.com?

For most of the time, specifically for the gapminder_hw01.Rmd file and README.md, I edited locally, saved, commited and pushed to Github. Each time I made sure to add comments when I made the commit to describe what changes were made.

- [x] How did it all work for the R Markdown document?
 
Yes everything worked fine with R Markdown. It was important for me to push ALL the files created locally on to github, including the images generated by knitting the R markdown file, so that the plots show up in the markdown file on Github.

