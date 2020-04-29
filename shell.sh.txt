#!/bin/bash
var1=$((RANDOM % 9))
echo "Please select a number between 1 to 10"
no_of_chances=1
for (( ; ; ))
do
        echo "Enter a number !"
        echo "This is your chance no $no_of_chances,Guess the number:"
  read var2

  if (( var2 == var1))

  then
        echo "Your guess is correct"
        echo "You win.Congratulations"
        echo "You guessed this with $no_of_chances chance/chances "
        echo "THANK YOU FOR PLAYING LEVEL1"
        echo "Yor are qualified for next level"
        break

        fi


if (( var2 > var1 ))

then
        echo "guess low number"
        echo "You are getting away from number"
        echo "The range is 1 to 10"

fi

if (( var2 < var1 ))
then
        echo "guess higher number"
        echo "You are close to the number"
        echo "The range is 1 to 10"
fi
no_of_chances=$((no_of_chances+1))


done