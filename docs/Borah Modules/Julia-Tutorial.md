# Julia Tutorial on R2 and Borah

This comprehensive guide will help you set up and use Julia, a high-level, high-performance programming language, on both R2 through Open OnDemand and Borah.

## Setting Up Julia on R2 through Open OnDemand

[Open OnDemand](https://openondemand.org/) provides users with a graphical interface to the cluster, currently available only for R2: [https://r2-gui.boisestate.edu](https://r2-gui.boisestate.edu).

### Step 1: Load the Julia Module
First, load any of the available Julia modules. You can see the available modules using \`module avail -i julia\` and load the desired module using \`module load julia/<version number here>\`.

```bash
$ module load julia
$ julia
```

You'll see your prompt change to the Julia terminal:

```bash
julia>
```

### Step 2: Install the IJulia Kernel
In the Julia terminal, install the IJulia kernel:

```julia
using Pkg
Pkg.add("IJulia")
```
(You'll only need to add the IJulia package once.)

### Step 3: Use Julia in a Jupyter Notebook
Navigate to the Jupyter Notebook App on [https://r2-gui.boisestate.edu](https://r2-gui.boisestate.edu), start a Jupyter session, and select the Julia kernel.

## Using Julia on Borah

### Step 1: Load the Julia Module
Borah uses "modules" to manage software. To use Julia, load its module:

```bash
module load julia
```

### Step 2: Confirm Julia Module is Loaded
Check that Julia is in the list of loaded modules:

```bash
module list
```

### Step 3: Create a Test File
Create a test file using \`vim\`:

```bash
vim test.jl
```

Write a simple Julia script to calculate the sum of two numbers:

```julia
# Function to calculate the sum of two numbers
function sum_numbers(a, b)
    return a + b
end

# Main program
println("Welcome to the Sum Calculator!")
println("Enter the first number:")
number1 = parse(Float64, readline())
println("Enter the second number:")
number2 = parse(Float64, readline())

# Calculate the sum and display the result
result = sum_numbers(number1, number2)
println("The sum of $number1 and $number2 is: $result")
```

### Step 4: Run the Test Using Julia
Execute the test script:

```bash
julia test.jl
```

## Extra Notes and Resources
1. [Julia Documentation](https://docs.julialang.org/): Comprehensive guides, tutorials, and references.
2. [Julia By Example](https://juliabyexample.helpmanual.io/): Practical examples of Julia programming.
3. [Julia Discourse](https://discourse.julialang.org/): Community forum to seek help, share ideas, and learn.
4. [JuliaHub](https://juliahub.com/): Platform hosting interactive Julia notebooks.
5. [Julia Academy](https://juliaacademy.com/): Online courses and tutorials to enhance your Julia skills.

This combined guide provides you with a step-by-step process for working with Julia on both R2 and Borah, from setting up the IJulia kernel to creating and running a basic script. Whether you're using Julia for scientific computing, data analysis, or machine learning, these instructions will get you started on both platforms.