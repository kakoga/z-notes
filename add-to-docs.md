ADD TO DOCUMENTATION

# TEMPLATE
## To create a dropdown in plate.xml:

    <templateset name="some_templateset" name_friendly="Some Templateset" view="a_templateset" parent_item="templateset_home">
    <fields>
      <dropdown name="some_dropdown" name_friendly="Some Dropdown" options="optionone:One;optiontwo:Two;" />
    </fields>
    <items>
      <item>
        <some_dropdown><![CDATA[optionone]]></some_dropdown>
      </item>
    </items>
    </templateset>

    Options for the dropdown must be key:value pairs separated by a semi-colon.

    If you want the dropdown to default to one of the options, then the key (of the key:value pair) in the CDATA tags as shown above. If you leave the CDATA tag
    blank then the dropdown will default to blank.

## toggle:
    yes_no togge is the same - just do options="0:Yes;1:No;"

## Parenting:
    parent vs. parent_item, which items need to be parented.

# PARSLEY

## If statements:
    If using a loose string it must be in quotes.
    Good:
     {{ if {page.title} == 'Home' }}

    Bad:
      {{ if {page.title} == Home }}  
  (technically both work, however it taxes the server much more without quotes)
  
## Each loops
    each loops, depending on the code, act as their own if-statement or has if-statement-like properties. 
