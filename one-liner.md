## Find duplicate ids in a locallang.xlf file

```
xmlstarlet sel -t  -m '/xliff/file/body/trans-unit' -n -v @id locallang.xlf | awk 'NF' | sort | uniq -c  | grep -v '^ *1 ' | sort -nr
```
