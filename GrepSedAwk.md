# Grep Sed Awk

## 1. 'Grep' - A
```
# -w ---> This option is used to match whole words only. (eg) Will matched line contains "the"  not "thee" or "thereby"
# -i ---> Ignore cases
# -E ---> This option enables extended regular expressions (act as egrep)

grep -Ewi 'the|that|then|those';
```
> OR
```
egrep -wi 'the|that|then|those';
```

## 2. 'Grep' - B
```
grep '\([0-9]\) *\1'

# \( and \)  are used to define a group in the regular expression
# [0-9]      matches any single digit.
# *          matches zero or more occurrences of the preceding element. In this case, it matches zero or more spaces.
# \1         refers to the first captured group (the digit within the parentheses). It ensures that the digit is repeated immediately after the optional spaces.
```

## 3. 'Grep' #1
```
grep -w "the"
```

## 4. 'Grep' #2
```
grep -wi "the"
```

## 5. 'Grep' #3
```
grep -vi "that"
```

## 6. 'Sed' command #1
```
Reason to add space is to avoid this kind of transform text ---- thereby >> thisreby
Input:   That thereby beauty's rose might never die,
Output:  That thisreby beauty's rose might never die,

sed -e s/"the "/"this "/
```

## 7. 'Sed' command #2
```
sed -e s/"thy "/"your "/ig
```

## 8. 'Sed' command #3
```
sed -e s/"thy"/{\&}/gi
```

## 9. 'Sed' command #4
```
sed -r 's/[0-9]{4}[ ]/**** /g'

# Pattern:
# [0-9]{4}  --> Four digit random number of 0,1,2,3,4,5,6,7,8,9
# []        --> a space
```

## 10. 'Sed' command #5
```
sed -r 's/([0-9]{4}) ([0-9]{4}) ([0-9]{4}) ([0-9]{4})/\4 \3 \2 \1/'
```

## 11. 'Awk' - 1
```
awk '{ if($4=="") print "Not all scores are available for " $1}'
```

## 12. 'Awk' - 2
```
# ternary expression - condition ? pass : fail
awk '{ print $1 ($2>=50 && $3>=50 && $4>=50 ? " : Pass" : " : Fail") }'
```
> OR
```
# ternary expression - condition ? pass : fail
awk '{ print $1 ($2<50 || $3<50 || $3<50 ? " : Fail" : " : Pass") }'
```

# 13. 'Awk' - 3
```
awk '{
    sum=$2+$3+$4
    avg=sum/3
    if (avg>=80) grade="A"
    else if (avg<80 && avg>=60) grade="B"
    else if (avg<60 && avg>=50) grade="C"
    else grade="FAIL"
    print $0 " : " grade }'
```

# 14. 'Awk' - 4
```
awk 'ORS=NR%2==0 ? "\n" : ";"'

# ORS stands for "Output Record Separator" in awk
# This allows you to control the separator between lines in the output.
```
