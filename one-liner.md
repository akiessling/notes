## Find duplicate ids in a locallang.xlf file

```
cat locallang.xlf | xmlstarlet sel -t  -m '/xliff/file/body/trans-unit' -n -v @id | awk 'NF' | sort | uniq -c  | grep -v '^ *1 ' | sort -nr
```
