# Bash
## 1. Let's Echo
```
echo "HELLO"
```

## 2. A Personalized Echo
```
read input;
echo "Welcome" $input
```

## 3. Looping with Numbers
```
for i in {1..50};
do
    echo $i;
done
```

## 4. The World of Numbers
```
read a 
read b
echo `expr $a + $b`
echo `expr $a - $b`
echo `expr $a \* $b`
echo `expr $a / $b`
```

## 5. Comparing Numbers
```
read a
read b
if [ $a -gt $b ]
then
    echo "X is greater than Y "
elif [ $a -lt $b ]
then
    echo "X is less than Y "
else
    echo "X is equal to Y "
fi
```

## 6. Getting started with conditionals
```
read a
case $a in
y)
    echo "YES"
    ;;
Y)
    echo "YES"
    ;;
n)
    echo "NO"
    ;;
N)
    echo "NO"
    ;;
*)
    echo "Invalid"
;;
esac
```

## 7. More on Conditionals
```
read x 
read y 
read z 

if [ $x -eq $y ] && [ $x -eq $z ];
then
    echo "EQUILATERAL"
elif [ $x -eq $y ] || [ $x -eq $z ] || [ $y -eq $x ] || [ $y -eq $z ] || [ $z -eq $x ] || [ $z -eq $y ]
then
    echo "ISOSCELES"
else
    echo "SCALENE"
fi
```

## 8. Looping and Skipping
```
for i in {1..99..2}
do
echo $i;
done
```
> OR

```
for ((i=1;i<=99;i=i+2))
do
echo "$i";
done
```

## 9. Arithmetic Operations
```
read a
printf %.3f $(echo "$a" | bc -l)
```

## 10. Compute the Average
```
read len;
sum=0;

for((i=1;i<=$len;i++))
do
read num
sum=`expr $sum + $num`
done

printf %.3f $(echo "scale=4; $sum / $len" | bc)
```
