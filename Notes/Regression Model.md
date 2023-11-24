### Linear Regression with One Variable
- **One variable**: single variable
	- **Univariate linear regression**
		- Means one variable also
- Predicts numbers
- Infinite amount of outcomes
- Terminology
	- **Training set**: data used to train the model
	- **Input variable**: values fed into model
		- Also called a **feature**
		- Notation: **x**
	- **Output variable**:
		- Also called a **target variable**
		- Notation: **y**
	- Number of training examples
		- Notation: **m**
		- Rows in data set
	- Single training example
		- Notation: **(x, y)**
		- A single row
		- Example: (2104, 400) -> row where x: 2104 and y: 400
	- ith training example
		- Notation: **(x^(i), y^(i))**
		- The ith row in the dataset
		- Not an exponent
	- **Model**: function created from training data
		- Takes in a new **x** and outputs a predicted **y**
		- Notation: ***f*
		- How to represent ***f*
			- What is the math formula we are going to use to compute *f*
		- **𝑓𝑤,𝑏(𝑥^(𝑖))=𝑤𝑥^(𝑖)+𝑏**
			- **w** - weight
			- **b** - bias
	- **Prediction**
		- Notation: **y-hat** - **ŷ**
		- Also called an estimate
		- Predicted value of **y**
		- When seeing only **y** that refers to the target

### NumPy and MatPlotLib Python exercise
- Creating a NumPy one-dimensional array: `x_train = np.array([1.0, 2.0])`
- NumPy Shape
	- `x_train.shape`: returns a python tuple with an entry for each dimension
	- `x_train.shape[0]` returns length of the array (number of examples)
	- Can also use `len(x_train)` to get length of array
- To retrieve **(x^i, y^i)**:
```
x_i = x_train[i]
y_i = y_train[i]
```
- Can plot examples using MatPlotLib.scatter 
```
import MatPlotLib as plt

temp_f_wb = compute_model_output(x_train, w, b)

# Plot our model prediction
plt.plot(x_train, tmp_f_wb, c='b',label='Our Prediction')
# Plot the data points
plt.scatter(x_train, y_train, marker='x', c='r')
# Set the title
plt.title('Housing Prices')
# Set y-axis label
plt.ylabel('Price (in 1000s of dollars)')
# Set x-axis label
plt.xlabel('Size (1000 sqft)')
plt.show()
```

### Cost function formula
- Will tell us how well the model is doing so we can try and get it to do better
- Regression model:
	- Model: `fwb(X) = wx + b`
		- `f(x)` as short hand
	- `w,b`: **parameters**
		- variables you can adjust in training to improve the model
		- also referred to as **coefficients** and **weights**
		- changes function and line on graph
	- Plotting `f(x)`
		- `w = 0, b = 1.5` 
			- chart has horizontal flat line
			- `f(x) = 0*x + 1.5` -> will always predict 1.5 - `ŷ = 1.5`
			- `b = y-intercept` because that's where it crosses the y-axis
		- `w = 0.5, b = 0`
			- `f(x) = 0.5*x + 0`
			- Standard slope of `0.5`
		- `w = 0.5, b = 1`
			- `f(x) = 0.5*x + 1`
			- Y-intercept of `1`
			- Slope of `0.5`
	- Does line fit the data?
		- The line of `fwb` roughly passes through the data points visually
	- Notation
		- `ŷ^(i) = fw,b(X^(i))`
		- 