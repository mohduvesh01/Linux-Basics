
# ✅ Day 6: File Searching & Filtering in Linux (For DevOps)

## 🎯 Goal:
Master searching and filtering files in Linux using commands like `find`, `locate`, `grep`, `cut`, `sort`, `uniq`, and `wc`.

---

## 📌 1. File Searching Commands

### 🔹 find – Search files by name, type, size, etc.
```bash
find /home -name "notes.txt"        # Find by name
find /var/log -name "*.log"         # Find by extension
find / -size +100M                  # Find by file size
find /etc -type d                   # Find by type (directory)
```

✅ Powerful but slower (scans the filesystem in real time).

---

### 🔹 locate – Search files instantly using database
```bash
sudo updatedb                       # Update database
locate notes.txt                    # Search quickly
locate *.log
```

✅ Very fast, but may not show newly created files until updated.

---

## 📌 2. File Content Searching (Filtering)

### 🔹 grep – Search text inside files
```bash
grep "error" /var/log/syslog        # Search
grep -i "error" /var/log/syslog     # Case-insensitive
grep -n "error" /var/log/syslog     # Show line numbers
grep -r "main()" /home/projects     # Recursive
```

✅ Supports regex for advanced filtering.

---

### 🔹 cut – Extract specific columns
```bash
cut -f1 data.txt                    # First column (tab delimited)
cut -d',' -f2 employees.csv         # Extract 2nd column from CSV
```

### 🔹 sort – Sort lines in a file
```bash
sort names.txt                      # Alphabetical sort
sort -n numbers.txt                 # Numeric sort
sort -r names.txt                   # Reverse sort
```

### 🔹 uniq – Remove duplicate lines
```bash
uniq names.txt                      # Unique lines
uniq -c names.txt                   # Count duplicates
```

### 🔹 wc – Word/line/character count
```bash
wc file.txt                         # Count lines, words, chars
wc -l file.txt                      # Line count only
```

---

## 📌 3. Combine Commands with Pipes (|)
```bash
grep "error" /var/log/syslog | wc -l                # Count "error"
cat file.txt | tr ' ' '\n' | sort | uniq -c | sort -nr | head -10   # Top 10 words
find /var/log -name "*.log" | xargs grep "failed"   # Search "failed" in all .log
```

---

## 📌 4. Practice Tasks (Hands-On)
1. Find all `.conf` files inside `/etc`.
2. Search for the word "failed" inside `/var/log/auth.log`.
3. Extract only usernames (first column) from `/etc/passwd`.
4. Sort a list of numbers and remove duplicates.
5. Count how many `.txt` files exist in your home directory.
