# College Departments & Majors

- `departments.json` — `schools` (id, name) and `departments` (id, name, schoolId) found at a typical four-year college or university.
- `majors.json` — undergraduate majors: `{ "id", "name", "departmentIds": [...] }`. A major that is commonly housed in more than one department lists every department ID.
- `majors/<id>.json` — one file per major with `summary` (2–4 sentences), `description` (up to 1000 characters) and `jobs` (an array of careers the major can lead to).
- `index.html` — an interactive page for browsing majors by department (search, expand/collapse, jump between shared departments). Clicking a major fetches only that major's `majors/<id>.json` and shows it in a modal.
- `colleges.json` — 140 accredited four-year US colleges and universities, including online-first universities: `id`, `name`, optional `short_name`, `city`, `state`, `undergraduates` (fall 2023 undergraduate headcount from the U.S. Department of Education's IPEDS data, rounded to the nearest thousand), `online_first` and `data_year`.
- `colleges/<id>.json` — one file per college with everything in `colleges.json` plus `homepage_url`, a 1–2 sentence `description`, and `mascot` (the athletic team name, when the school has one).
- `colleges.html` — a sortable, searchable table of `colleges.json`, filterable by state and by campus-based or online-first. Clicking a college fetches only that college's `colleges/<id>.json` and shows it in a popup.

To view the pages locally, serve this folder (browsers block `fetch()` from `file://`):

```sh
python3 -m http.server
# then open http://localhost:8000
```
