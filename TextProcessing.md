# Text Processing

## Cut #1
```
cut -c 3
```
> OR
```
cut -b 3
```

## Cut #2
```
cut -c 2,7
```

## Cut #3
```
cut -c 2-7
```

## Cut #4
```
cut -c 1-4
```

## Cut #5
```
cut -d $'\t' -f 1-3
```

## Cut #6
```
cut -c 13-
```

## Cut #7
```
cut -d ' ' -f 3
```

## Cut #8
```
cut -d " " -f 1-3
```

## Cut #9
```
cut -d $'\t' -f 2-
```

## Head of a Text File #1
```
head -20
```

## Head of a Text File #2
```
head -c 20
```

## Middle of a Text File
```
head -22|tail +12
```

## Tail of a Text File #1
```
tail -20
```

## Tail of a Text File #2
```
tail -c 20
```

## 'Tr' Command #1
```
tr "()" "[]"
```

## 'Tr' Command #2
```
tr -d "[a-z]"
```

## 'Tr' Command #3
```
tr -s " "
```

## Sort Command #1
```
sort
```

## Sort Command #2
```
sort -r
```

## Sort Command #3
```
sort -n
```

## Sort Command #4
```
sort -rn
```

## Sort Command #5
```
sort -t $'\t' -rnk 2
```

## Sort Command #6
```
sort -t $'\t' -nk 2
```

## Sort Command #7
```
sort -t '|' -rnk 2
```

## 'Uniq' Command #1
```
uniq
```

## 'Uniq' Command #2
```
uniq -c | sed -e s/^[[:space:]]*/""/
```
