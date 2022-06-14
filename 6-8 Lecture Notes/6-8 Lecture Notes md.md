# 6-8 Lecture Notes

# Continuing on Data Wrangling

join

- combines two tables based on common variables
- two tables are called
    - left table
    - right table
- steps to combine table
    - identify common variables
    - create a new table with variables from both tables
    - add values from rows according to the specific type

**faster in memory, but volatile**

join types:

- inner_join() - retain (only) observations where this is a match in both datasets (left and right
- left_join() - Keep all rows in left-hand dataset, add values from right-hand dataset where there is a match.
    - For non-matching observations, fill in NA
- right_join() -Keep all rows in right-hand dataset, add values from left-hand dataset where there is a match
    - For non-matching observations, fill in NA
- full_join() - Combine observations from both datasets based on matching key and fill in NA for non-matches

filter join types:

- creates a new table with variables from only left table (including common variables)
    - semi_join()
        - return all rows from LEFT where there are matching values in the RIGHT, keeping just columns from LEFT
    - anti_join()
        - returns all rows from LEFT where there are **NOT** matching vals in RIGHT, keeping columns from left