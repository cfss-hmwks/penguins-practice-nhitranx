## R Markdown

Here we are going to learn a bit about penguins!

## Penguins

See below for averages on penguins.

    ## # A tibble: 3 × 3
    ##   sex    avg_bill avg_mass
    ##   <fct>     <dbl>    <dbl>
    ## 1 female     37.3    3369.
    ## 2 male       40.4    4043.
    ## 3 <NA>       37.8    3540

## Your work

Summarize the dataset in a meaningful way (use AT LEAST two of the key
functions from slide \#12)

    penguins %>%
      filter(sex == "female") %>%
      group_by(island) %>%
      summarize(avg_bill_length = mean(bill_length_mm, na.rm = TRUE),
                avg_bill_depth = mean(bill_depth_mm, na.rm = TRUE),
                avg_mass = mean(body_mass_g, na.rm = TRUE))

    ## # A tibble: 3 × 4
    ##   island    avg_bill_length avg_bill_depth avg_mass
    ##   <fct>               <dbl>          <dbl>    <dbl>
    ## 1 Biscoe               43.3           15.2    4319.
    ## 2 Dream                42.3           17.6    3446.
    ## 3 Torgersen            37.6           17.6    3396.

# Final task

You need to make a README.md doc – practice by outputting a .md file
here and renaming it to README.md before pushing to github
