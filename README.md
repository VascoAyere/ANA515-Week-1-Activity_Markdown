# ANA515-Week-1-Activity_Markdown
This is ANA 515_01 week R activity.

 # title: "Diamond sizes"
#author: Vasco_Ayere_Avoka
#date: 2023
#output: word_document

  # Setup Code Chunk  ---- 
library(ggplot2)
library(dplyr)

# Data Preparation  ----
smaller <- diamonds %>%
  filter(carat <= 1)

# Inline Code   ---
n_diamonds <- nrow(diamonds)
n_smaller <- nrow(smaller)
n_larger <- n_diamonds - n_smaller

# Create Plot ----
smaller %>%
  ggplot(aes(carat)) +
  geom_freqpoly(binwidth = 0.01)
