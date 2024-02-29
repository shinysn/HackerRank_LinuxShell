# Text Processing

## 1. Cut #1
```
cut -c 3
```
> OR
```
cut -b 3
```

## 2. Cut #2
```
cut -c 2,7
```

## 3. Cut #3
```
cut -c 2-7
```

## 4. Cut #4
```
cut -c 1-4
```

## 5. Cut #5
```
cut -d $'\t' -f 1-3
```

## 6. Cut #6
```
cut -c 13-
```

## 7. Cut #7
```
cut -d ' ' -f 3
```

## 8. Cut #8
```
cut -d " " -f 1-3
```

## 9. Cut #9
```
cut -d $'\t' -f 2-
```

## 10. Head of a Text File #1
```
head -20
```

## 11. Head of a Text File #2
```
head -c 20
```

## 12. Middle of a Text File
```
head -22|tail +12
```

## 13. Tail of a Text File #1
```
tail -20
```

## 14. Tail of a Text File #2
```
tail -c 20
```

## 15. 'Tr' Command #1
```
tr "()" "[]"
```

## 16. 'Tr' Command #2
```
tr -d "[a-z]"
```

## 17. 'Tr' Command #3
```
tr -s " "
```

## 18. Sort Command #1
```
sort
```

## 19. Sort Command #2
```
sort -r
```

## 20. Sort Command #3
```
sort -n
```

## 21. Sort Command #4
```
sort -rn
```

## 22. Sort Command #5
```
sort -t $'\t' -rnk 2
```

## 23. Sort Command #6
```
sort -t $'\t' -nk 2
```

## 24. Sort Command #7
```
sort -t '|' -rnk 2
```

## 25. 'Uniq' Command #1
```
uniq
```

## 26. 'Uniq' Command #2
```
uniq -c | sed -e s/^[[:space:]]*/""/
```
> OR
```
uniq -c | cut -c 7-
```

## 27. 'Uniq' Command #3
```
uniq -ic | sed -e s/^[[:space:]]*/""/
```
> OR
```
uniq -ic | cut -c 7-
```

## 28. 'Uniq' command #4
```
uniq -u
```

## 29. Paste - 1
```
paste -s -d ";"
```

## 30. Paste - 2
```
paste - - - -d ";"
```

## 31. Paste - 3
```
paste -s -d $'\t'
```

## 32. Paste - 4
```
paste - - - -d $'\t'
```
