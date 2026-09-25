# College Departments & Majors

- `departments.json` — `schools` (id, name) and `departments` (id, name, schoolId) found at a typical four-year college or university.
- `majors.json` — undergraduate majors: `{ "id", "name", "departmentIds": [...] }`. A major that is commonly housed in more than one department lists every department ID.
- `majors/<id>.json` — one file per major with `summary` (2–4 sentences), `description` (up to 1000 characters) and `jobs` (an array of careers the major can lead to).
- `index.html` — an interactive page for browsing majors by department (search, expand/collapse, jump between shared departments). Clicking a major fetches only that major's `majors/<id>.json` and shows it in a modal.

To view the page locally, serve this folder (browsers block `fetch()` from `file://`):

```sh
python3 -m http.server
# then open http://localhost:8000
```
