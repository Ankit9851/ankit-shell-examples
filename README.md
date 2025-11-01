# ankit-shell-examples
shell scripts example projects 
📂 File: calculator.sh
#!/bin/bash

echo "==============================="
echo "     Simple Calculator"
echo "==============================="

# Taking input
read -p "Enter first number: " num1
read -p "Enter second number: " num2

echo "Choose Operation:"
echo "1) Addition (+)"
echo "2) Subtraction (-)"
echo "3) Multiplication (*)"
echo "4) Division (/)"
read -p "Enter choice (1-4): " choice

case $choice in
    1)
        result=$((num1 + num2))
        echo "Result: $num1 + $num2 = $result"
        ;;
    2)
        result=$((num1 - num2))
        echo "Result: $num1 - $num2 = $result"
        ;;
    3)
        result=$((num1 * num2))
        echo "Result: $num1 * $num2 = $result"
        ;;
    4)
        if [ $num2 -eq 0 ]; then
            echo "Error: Division by zero not allowed!"
        else
            result=$((num1 / num2))
            echo "Result: $num1 / $num2 = $result"
        fi
        ;;
    *)
        echo "Invalid option selected!"
        ;;
esac
▶️ How to run
chmod +x calculator.sh
./calculator.sh
