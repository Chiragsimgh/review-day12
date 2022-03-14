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
#! /bin/bash -x

temp=0
rem=0
orgNum=0
returnValue=0


function checkPalindrom(){
	while [ $firstNum -gt 0 ]
	do
		rem=$(( $firstNum % 10 ))
		firstNum=$(( $firstNum / 10 ))
		temp=$(( $(($temp * 10))+ $rem ))
	done
	echo $temp
}


read -p "Enter count of number check " count

while [ $count -gt 0 ]
do
	read -p "Enter the first number " firstNum
	orgNum=$firstNum

	returnValue=`checkPalindrom`

	if [ $returnValue -eq $orgNum ]
	then
		echo "Is palindrom"
	else
		echo "Not a palindrom"
	fi
((count--))
done



