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
* *type* is the type of the
