# oracle-apex-progress-status-region-plugin
An oracle APEX region plugin to show progress status

Demo
https://kjwvivmv0n5reuj-apexkqor.adb.uk-london-1.oraclecloudapps.com/ords/r/test1/plugin/home?session=105323527211920

Show users the status of a process in your Oracle APEX application

* Steps defined in your SQL
* Each step has a link to a page in your application. Clicking on step 2 takes you to page 2
* Animate steps in the process to indicate to users they should click on the step. In this   
  example we want to highlight to the user we want them to click on step 3.
* The animation can be changed in attributes.
* Tooltips are displayed when hovering over the step.
* Colours can be changed using the plugin attributes

Instructions 
---------------------------------------------------
Download the plugin

Install the plugin - Shared Components->plugins->import

Create a new region with type progress-status

Change source type to SQL Query then copy the demo SQL in.

Default SQL uses page 1 and 2 for linking, ensure what you put here exists so linking works.

You can leave attributes blank to start as it will use default settings.

Demo SQL
---------------------------------------------------
select 'Step 1','Tooltip 1', 1, '1', 0 from dual

union

select 'Step 2','Tooltip 2', 1, '2', 0 from dual

union

select 'Step 3','Tooltip 3', 0, '1', 1 from dual

union

select 'Step 4','Tooltip 4', 0, '2', 0 from dual

union

select 'Step 5','Tooltip 5', 0, '2', 0 from dual

union

select 'Step 6','Tooltip 6', 0, '2', 0 from dual


Attributes
---------------------------------------------------
onBackgroundColor - background colour of the on state

onTextState - text colour of the on state

offBackgroundColor - background colour of the off state

offTextState - text colour of the off state

animate - animation to use see animate (defaults to shakeX)


