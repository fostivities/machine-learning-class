### Learning objectives
- Define machine learning
- Define supervised learning
- Define unsupervised learning
- Write and run Python code in Jupyter Notebooks
- Define a regression model
- Implement and visualize a cost function
- Implement a gradient descent
- Optimize a regression model using gradient descent

### Overview of Machine Learning
- Subfield of AI
- Artificial General Intelligence (AGI) - AI dream – machines as intelligent as humans
	- Overhyped and a long way away from it
	- Researchers believe learning algorithms is best way to get to this goal
- State of AI in 2020 - Study by McKenzie
	- AI/ML $13t in value annually by 2030
- Vast unfulfilled demand for this skillset

### Supervised vs. Unsupervised Machine Learning
- Field of study that gives computers the ability to learn without being explicitly programmed.
	- Arthur Samule (1959)
- Two main types of ML
	- Supervised learning
		- Used most in real-world applications
		- Seen most rapid advancements
		- Course 1, 2
	- Unsupervised learning
		- Course 3
		- recommender systems and reinforcement learning

### Supervised learning
- Refers to algorithms that learn:
	- From x to y
	- Or input to output labels
- Learns from given "right answers"
	- Learns given a known output for a given input
	- Eventually just learns to take the input alone
- Examples:

| Input | Output | Application |  
| -------- | -------- | -------- |  
| email | span? | spam filtering |  
| audio | text transcripts | speech recognition |
| English | Spanish | machine translation |
| ad, user info | click on ad? | online advertising |
| image, radar info | position of other cars | self-driving car |
| image of phone | defect | visual inspection |

- 2 types of supervised learning algorithms
	- **Regression**: predict a number from infinitely many possible outputs
	- **Classification**: predict categories from a small number of outputs
		- Predicting a small amount of categories (vs regression that predicts any number out of any possible output)
		- Outputs are called classes or categories
		- Creates some sort of boundary from the categories


### Unsupervised learning
- Most widely used form of ML
- Given data that doesn't have a labeled output
	- Data comes with inputs x, but not output labels y
	- Algorithm has to find structure of data
- Goal is to find something interesting in unlabeled data
	- What patterns or structures are in this data?
- Types of unsupervised learning
	- **Clustering**:  places unlabeled data into clusters
		- Examples:
			- Google news - given a news articles for the day, groups related stories together
			- Grouping customers - group customers into different market segments
	- **Anomaly detection***: used to detect unusual events (find unusual data points)
	- **Dimensionality reduction**: compress a large data set into a smaller data set without losing information

### Jupyter Notebooks
- Default environment for many to experiment
- Web browser based environment
- Cells
	- Markdown cell - a bunch of text
	- Code cell - used to run code (shift + enter will run it)