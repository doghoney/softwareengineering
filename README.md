# GFM extension
----
## tables
- terms
  1. row
  2. column
  3. header row
  4. delimiter row
- use
  - basic
        | name | age |
        | ---- | --- |
        | junho | 21 |
  
  - using (:)
        | name | age |
        | :-: | ---------: |
        | junho | 21 |     
- escaping (\|)
    | f\|oo |
    | ----- |
    | b`\|` az |
    
  > \| -> |
  > `\|` -> <code>|<code>
- break
  > table is broken at the first empty line, or beginning of another block-level structure
  
- precautions
  >The header row must match the delimiter row in the number of cells.
    | abc | def |
    | --- |
    | bar |
  - this is treated as paragraph
- exception
  > if fewer than header row:
  > empty cells are inserted.
  > if greater than header row:
  > the excess is ignored

## task list items

## strikethrough

## Autolinks

## Disallowed Raw HTML

