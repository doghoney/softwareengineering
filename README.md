# GFM extension  
----  
## tables   
- terms  
  1. header row  
    \- top row
  2. delimiter row  
    |------|------|
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
  > `\|` -> \<code>|\<code>  
- break  
  > table is broken at the first empty line, or beginning of another block-level structure  
  
- precautions  
  >The header row must match the delimiter row in the number of cells.  

    | abc | def |  
    | --- |  
    | bar |  
  - this is treated as paragraph  
- exception  
  - fewer than header row:  
    \- empty cells are inserted.  
  - greater than header row:  
    \- the excess is ignored  
  - no rows  
    \- no \<tbody> is generated in HTML output  
## task list items
  - term
    1. task list items
    \- check box
  - use
    -basic 
        \- [ ] walk dog 
        \- [x] do homework
    - nested
        \- [x] today homework
          \- [ ] math
          \- [ ] english
        \- [ ] take a walk
        
## strikethrough

## Autolinks

## Disallowed Raw HTML

