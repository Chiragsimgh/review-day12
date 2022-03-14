# review-day12
#1.Program to short an array in descending order:-


#!/bin/bash
echo "enter maximum number"
read n
# taking input from user
echo "enter  Numbers in array:"
for (( i = 0; i < $n; i++ ))
do
read nos[$i]
done
#printing the number before sorting
echo "  Numbers in an array are:"
for (( i = 0; i < $n; i++ ))
do
echo ${nos[$i]}
done
# Now do the Sorting of numbers
for (( i = 0; i < $n ; i++ ))
do
for (( j = $i; j < $n; j++ ))
do
if [ ${nos[$i]} -lt ${nos[$j]}  ]; then
t=${nos[$i]}
nos[$i]=${nos[$j]}
nos[$j]=$t
done

# Printing the sorted number in descending order
echo -e "\nSorted Numbers "
for (( i=0; i < $n; i++ ))
do
echo ${nos[$i]}
done


#2. check if the number is palindrome or not:



