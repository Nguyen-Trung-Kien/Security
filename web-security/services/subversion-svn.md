# Subversion (SVN)

Search

```
// Some code
```

## Exploit

```
- wget file/

sqlite3 wc.db 'select local_relpath, ".svn/pristine/" || substr(checksum,7,2) || "/" || substr(checksum,7) || ".svn-base" as alpha from NODES;' | tee Snv_Database

cat Snv_database.txt | cut -d"|" -f2 | sort -u | sed "s/^/https:\/\/redacted.com\//" | tee Urls_generated.txt

Source code in:
- https://hosst/.svn/pristine/b8/b8a0e3681d[id]db4093bb35f15.svn-base

```
