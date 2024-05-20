Fahim Ashraf:
#!/bin/bash

echo "Enter the month (1-12): "
read month

echo "Enter the day (1-31): "
read day

echo "You entered $month and $day"

4.

#!/bin/bash

echo "Enter the first number: "
read num1

echo "Enter the second number: "
read num2

echo "Enter the third number: "
read num3

echo "Enter the fourth number: "
read num4

if [ $num1 -gt $num2 ] && [ $num1 -gt $num3 ] && [ $num1 -gt $num4 ]; then
  echo "$num1 is the biggest number"
elif [ $num2 -gt $num3 ] && [ $num2 -gt $num4 ]; then
  echo "$num2 is the biggest number"
elif [ $num3 -gt $num4 ]; then
  echo "$num3 is the biggest number"
else
  echo "$num4 is the biggest number"
fi

5.

#!/bin/bash

sum_forward=0
sum_reverse=0

# Forward sum
for (( i=100; i<=200; i++ ))
do
    if (( i % 9 == 0 )); then
        sum_forward=$((sum_forward + i))
    fi
done

# Reverse sum
for (( i=200; i>=100; i-- ))
do
    if (( i % 9 == 0 )); then
        sum_reverse=$((sum_reverse + i))
    fi
done

echo "Forward sum of numbers between 100 and 200 divisible by 9: $sum_forward"
echo "Reverse sum of numbers between 100 and 200 divisible by 9: $sum_reverse"

7.

#!/bin/bash

echo "Enter the first number: "
read num1

echo "Enter the second number: "
read num2

echo "Enter the third number: "
read num3

if [ $num1 -gt $num2 ] && [ $num1 -gt $num3 ]; then
  largest=$num1
elif [ $num2 -gt $num1 ] && [ $num2 -gt $num3 ]; then
  largest=$num2
else
  largest=$num3
fi

if [ $num1 -lt $num2 ] && [ $num1 -lt $num3 ]; then
  smallest=$num1
elif [ $num2 -lt $num1 ] && [ $num2 -lt $num3 ]; then
  smallest=$num2
else
  smallest=$num3
fi

echo "The smallest number is $smallest"
echo "The largest number is $largest"

3

#!/bin/bash

# Display the name and ID of the current user
echo "User name: $(whoami)"
echo "User ID: $$"

# Display the current date and calendar
echo "Date: $(date)"
echo "Calendar: $(cal)"

# Display CPU information
echo "CPU Information: $(lscpu)"

# Display all running processes
echo "Running processes:"
ps -ef

# Display the related status of CPU and memory
echo "CPU and memory usage:"
top -b -n1

1

#!/bin/bash

# Check if the correct number of arguments are provided
if [ "$#" -ne 3 ]; then
    echo "Usage: $0 num1 num2 num3"
    exit 1
fi

# Assign the command-line arguments to variables
num1=$1
num2=$2
num3=$3

# Find the minimum of the three numbers
if [ $num1 -le $num2 ] && [ $num1 -le $num3 ]; then
    min=$num1
elif [ $num2 -le $num1 ] && [ $num2 -le $num3 ]; then
    min=$num2
else
    min=$num3
fi

# Print the minimum value
echo "The minimum value is: $min"
3
