# College Departments & Majors

- `departments.json` — `schools` (id, name) and `departments` (id, name, schoolId) found at a typical four-year college or university.
- `majors.json` — undergraduate majors: `{ "id", "name", "departmentIds": [...] }`. A major that is commonly housed in more than one department lists every department ID.
- `index.html` — an interactive page for browsing majors by department (search, expand/collapse, jump between shared departments).

To view the page locally, serve this folder (browsers block `fetch()` from `file://`):

```sh
python3 -m http.server
# then open http://localhost:8000
```
