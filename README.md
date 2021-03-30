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
  > \`\|\` -> \<code>|\<code>  
- break condition  
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
  - basic 
       
        \- [ ] walk dog   
        \- [x] do homework  
  - nested
          
        \- [x] today homework  
          \- [ ] math  
          \- [ ] english  
        \- [ ] take a walk  
      
## strikethrough  
- term  
  1. strikethrough  
    ~~[Text]~~  
- use  
   - basic
          
        \~\~Hi\~\~ Hello, World!  
- caution  
  > new paragraph will cause strikethrough parsing to cease  
   
      This ~~ has a  
      new paragraph~~.  
## Autolinks  
- term  
  1. Autolinks  
    \-automatically recognize and make into link  
- URL  
  > http will be inserted automatically  
  1. vaild domain  
  
        www.naver.com    
  2. zero or more non-space non-< characters may follow  
        
        Visit www.commonmark.org/help for more information.  
  3. Trailing punctuation (specifically, ?, !, ., ,, :, *, _, and ~) will not be considered  
        
        Visit www.commonmark.org.  
    - only "www.commonmark.org" is considered as link
  4. autolink ends in )  

        www.google.com/search?q=Markup+(business)))  
    - automatically consider as "www.google.com/search?q=Markup+(business)"  
  
  5. autolink ends in a semicolon(;)  
  
        www.google.com/search?q=commonmark&hl;  
    - exclude entitiy reference (after &)  
    - automatically consider as "www.google.com/search?q=commonmark"  
  6. '<' immediately ends an autolink  

        www.commonmark.org/he<lp  
    - automatically consider as "www.commonmark.org/he"   
  7. http://, https://  
  
        http://commonmark.org  
        https://commonmark.org  
        
- email
  >1\. One ore more characters which are alphanumeric, or ., -, _, or +.  
  >2. An @ symbol.   
  >3. One or more characters which are alphanumeric, or - or _, separated by periods (.).    
  >4. There must be at least one period. The last character must not be one of - or _.     
  >5. + can occur before the @, but not after.     
  >6. ., -, and _ can occur on both sides of the @, but only . may occur at the end of the email address, in which case it will not be considered part of the address:  
    
  - basic  
  
        foo@bar.baz  
  
## Disallowed Raw HTML
>GFM enables the tagfilter extention
>But, some HTML tag is not allowed
  - \<title>
  - \<textarea>
  - \<style>
  - \<xmp>
  - \<iframe>
  - \<noembed>
  - \<noframes>
  - \<script>
  - \<plaintext>

        <strong> <title> <style> <em>

        <blockquote>
          <xmp> is disallowed.  <XMP> is also disallowed.
        </blockquote>

    >\<p>\<strong> \&lt;title> \&lt;style> \<em>\</p>  
    >\<blockquote>  
    >\&lt;xmp> is disallowed.  \&lt;XMP> is also disallowed.  
    >\</blockquote>  
