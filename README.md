
#!/bin/bash

# Function to calculate simple interest
calculate_interest() {
    principal=$1
    rate=$2
    time=$3
    # Calculate simple interest using the formula I = (P * R * T) / 100
    # Use bc for floating-point arithmetic
    interest=$(echo "scale=2; ($principal * $rate * $time) / 100" | bc)
    echo "Simple Interest: $interest"
}

# Prompt user for input
read -p "Enter Principal Amount (P): " principal_input
read -p "Enter Rate of Interest (R): " rate_input
read -p "Enter Time Period (T) in years: " time_input

# Call the function with user input
calculate_interest $principal_input $rate_input $time_input
