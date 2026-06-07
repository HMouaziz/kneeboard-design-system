# Page Spec Template

Use this after aircraft content is normalized and before rendering HTML.

```yaml
page:
  aircraft: ""
  title: ""
  subtitle: ""
  style: ""
  format: ""
  page_number: 1
  page_count: 1
  density: "normal"
  columns: 1
  header:
    left: ""
    center: ""
    right: ""
  footer:
    left: ""
    center: ""
    right: ""
  sections:
    - title: ""
      section_type: ""
      importance: "normal | major | minor"
      rows: []
  diagrams: []
  qa_notes: []
```

## Required decisions

Before rendering, decide:

```txt
style
format
page title
page density
one column or two columns
which sections are on this page
which rows are critical/muted/optional
which notes are kept, shortened, or moved
```
