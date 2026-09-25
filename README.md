# College Departments & Majors

- `departments.json` — `schools` (id, name) and `departments` (id, name, schoolId) found at a typical four-year college or university.
- `majors.json` — undergraduate majors: `{ "id", "name", "departmentIds": [...] }`. A major that is commonly housed in more than one department lists every department ID.
- `majors/<id>.json` — one file per major with `summary` (2–4 sentences), `description` (up to 1000 characters) and `jobs` (an array of careers the major can lead to).
- `index.html` — an interactive page for browsing majors by department (search, expand/collapse, jump between shared departments). Clicking a major fetches only that major's `majors/<id>.json` and shows it in a modal.
- `colleges.json` — the 100 largest accredited four-year US colleges by undergraduate enrollment, including online-first universities: `id`, `name`, optional `short_name`, `city`, `state`, `undergraduates` (rounded to the nearest thousand), `online_first`, `included_for` and `data_year`. Entries 101+ (`included_for: "us_news_top_50"`) are smaller schools added because they rank in the US News top 50 national universities (2026 edition).
- `colleges.html` — a sortable, searchable table of `colleges.json`, filterable by state and by campus-based or online-first.

To view the pages locally, serve this folder (browsers block `fetch()` from `file://`):

```sh
python3 -m http.server
# then open http://localhost:8000
```
