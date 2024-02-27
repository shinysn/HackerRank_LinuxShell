# Arrays in Bash

## 1. Read in an Array
```
i=1
while read a 
do
    country[i]=$a
    i=`expr $i + 1`
done

echo ${country[@]}
```

## 2. Slice an Array
```
i=0
j=0
while read a
do
    if(($i>=3 && $i<=7))
    then
        country[j]=$a
        j=`expr $j + 1`
    fi
    i=`expr $i + 1`
done

echo ${country[@]}
```

## 3. Filter an Array with Patterns
```
while read a
do    
    if (echo $a|grep -iqv a)
    then
        country=(${country[*]} $a)
    fi
done

echo ${country[@]}
```

## 4. Concatenate an array with itself
```
country=($(cat))
country=(${country[@]} ${country[@]} ${country[@]})
echo ${country[@]}
#country=("${country[@]}" "${country[@]}" "${country[@]}")
```

## 5. Display an element of an array
```
country=($(cat))
echo ${country[3]}
```

## 6. Count the number of elements in an Array
```
country=($(cat))
echo ${#country[@]}
```

## 7. Remove the First Capital Letter from Each Element
```
i=0
while read a
do
    country[i]=`echo $a|sed -e s/^"[a-z]"/"."/gi`
    i=`expr $i + 1`
done

echo ${country[@]}
```

## 8. Lonely Integer - Bash!
```
read len
number=($(cat))

echo "${number[@]}"|tr ' ' '\n'|sort|uniq -u
```
