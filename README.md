# Notes-for-setting-up-a-css-refactor-process
objectives, obstacles, the process for solution, discussion - things to consider when simplifying css.

## Objectives:
1) css ClassNames should be as explicit as an inline style 
<br/>the purpose of classNames should be to remove repetition.
<br/>id's should describe grouping of html for the app.
2) 

## Obstacles:
1)classNames for bad css are not your friend ... 
<br/>they often have dead code  
<br/>and hide the styling relationship between html elements.
2) 

## The process for solution:
1) copy the file to create a backup file.
2) copy the file to another file with all of the classNames and no styles inside the names.
3) copy the file to another file where you can find and replace to switch the css to an inline format.
<br/>Use this file to get all of the formatting consistent such as always `"color: blue;" instead of:
```
"color: blue;"
"color:blue;"
"color: blue"
```
4) Now search the key names of the inlinecss file. 
<br/>and when 1 of "num"... write down "num" for that element.
<br/>this exposes the amount of duplication for each css element.


## Process for solution, final steps: 
1) write all of the css as inline styles... keep the classNames.
(should not break anything since the same classNames are used).
2) switch the css file to the empty css file. 
<br/>(should not break anything since you now have styles inline).
3) using dev tools remove all the dead css.
4) now with all inline styles next to each other attempt to simplify the inline styles.
5) copy the css file with empty classNames to one for inline style translation.
6) rewrite the inline styles back into the css file with empty classNames, using find and replace.
7) switch to the new css file and congratulate yourself ... pray that nothing is broken 
<br/>and consider writing more tests over styling.
8) check tachyons for a class to replace repeated css: https://cdnjs.cloudflare.com/ajax/libs/tachyons/4.11.1/tachyons.css
<br/>... copy the response from the tachyons link to a css file format with a code formatter 
<br/>... then search based on css class. whoa you did not find a css class that could remove the duplication 
<br/>... no worries make a global css class for your project ... but wait! check tachyons before hand by searching that name. It exists in tachyons pick a different name. Example: `padding: absolute` 🤔 ... hmm. class: pa! Searching pa in tachyons... we are good. put in the global css file brought in by index.html.

# Anything to add? open an issue or submit a pr!
