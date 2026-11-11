## 2024-05-24 - JSON Parsing in SQLite Updates
**Learning:** In SQLite, appending to a JSON array column by reading, parsing (JSON.parse), pushing, and stringifying (JSON.stringify) in Node.js scales poorly as the array grows, leading to O(N^2) behavior for N appends. Using SQLite's built-in `json_insert(column, '$[#]', json(?))` is significantly faster.
**Action:** Use `json_insert` for appending to JSON arrays in SQLite columns to avoid read-parse-stringify roundtrips.
