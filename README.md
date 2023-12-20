This is my solution to the **Engineering Prompt** for the **2023 Sports Reference Internship Application**.

My solution is written in Python and uses both `pandas` and `json` libraries. The project is implemented in a Jupyter Notebook and is commented out for better readability.

## Running the code
Open the `main.ipynb` and `stats.json` files in a Jupyter Notebook to run the code. A table with the team records will be returned. 

## Explanation
My solution involves opening a JSON file to fetch each team record and calling a function to turn that data into a table using pandas.

My solution involves opening the given JSON file to grab the team record data and is put into the `create_table` function where the table is generated.

In this function, a table is created with the JSON data but with incorrect values for each cell. To fix this, first I set each column and row index to names of the teams in the data. Then, I used a for-loop to iterate through a list of the teams (defined as team) and a nested for-loop to do the same within each team (defined as opponent). Inside our nested for-loop, I would check to make sure that the team was not the same as the opponent. If it wasn't, I set the cell aligned with the two teams to the amount of wins by our team against the opponent. If it was, I didn't change the cell to a record and left it as a string.

After repeating this action for each team against each opponent, I returned the full table and then used the `head` function so that the table could be viewed. 