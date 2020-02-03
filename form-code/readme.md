# Form Code Generator

When I was writing validating JS code for a certain form on our company's website, [FirstEdge Electronics](firstedge.co.zw), I noticed two things:
* It was boring
* I have done that kind of thing before
So I decided to make my task more interesting. Then I came with an idea of creating a tool to automate the boring stuff. All I wanted was to tell it the kind of form that I want, at it will produce the code for me
Here is the format(It's JSON):

```
	{
		"type" : string,
		"can_be_empty": boolean,
		"attributes": {
			 string : string,  // attribute name-value pair
       ...
		},
		"needs_confirm": boolean,
		"format": {
			"regex": string,
			"error_msg" : string
		},
		"label": string,
		"accepts": [string, ...]
	}
```

Explaination of the JSON object above:
* *type* is the type of the element we wish to add in the form
   * textbox
   * password-box
   * option-box
   * button
   * *multi-line*: a multiline textbox, textarea in HTML terms 
  We have to put the type typed exactly as typed above. Don't try to be smart and use things like "input" for textbox as in HTML, it will not work.
* *can_be_empty* indicates if the user is allowed not to fill this element when filling in the form.
* *atrributes*: Attributes of the elements in the actual HTML sense. Please note that the 
