## Find duplicate ids in a locallang.xlf file

```
cat locallang.xlf | xmlstarlet sel -t  -m '/xliff/file/body/trans-unit' -n -v @id | awk 'NF' | sort | uniq -c  | grep -v '^ *1 ' | sort -nr
```

## extract urls from a sitemap.xml (only one file, no support for split up sitemaps)

```
xmlstarlet sel -t -v '//*[local-name()="loc"]' sitemap.xml |sed 's/ *//g' 
```
Kudos to http://p.cweiske.de/357

or directly from an online sitemap:
```
curl -s https://www.sitemaps.org/sitemap.xml | xmlstarlet sel -t -v '//*[local-name()="loc"]'  | sed 's/ *//g'
```
