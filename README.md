#Front-end Coding Standards
##HTML
- Use HTML5 
- Try to keep markup semantic
- 	ie: use p tags instead of span + br tags for body text, etc...
- Use double quotes for attributes
- Information can be kept in mark up as attributes 
-- eg: <div class="user" data-user-pk="1" data-name="Aris"></div>
- Forms
- 	Use label fields to label each form field, the for attribute should associate itself with the input field
- Tables are for tabular data, not forms/layout/etc...
	

##CSS
- No inline-CSS or <style></style> tags.
- 	Ever.
- No IDs in CSS selectors
- 	They are fine for use in JS but not in our style sheets
- No markup in CSS selectors. 
- 	If you want to style something, give it a class. 
- 	.user h3{} /* this is bad */
- 	.user .userName {} /* this is better */
- We should use a hybrid of BEM and OOCSS principles
- 	A block is the smallest 
- Class naming
- 	describe what the class *is* rather than what it *looks like*
- 		.bigText /*Bad*/
- 		.recognitionNominee /*Good*/
- 	camelCaseYourClassNames
- Avoid !important, unless absolutely necessary
- Only set widths on containers/wrappers
- 	Wrappers with explicit width should have NO padding
- You shouldn't be setting heights, but if you need to:
- 	make sure it's only on a wrapper element
- 	specify an overflow
- use floats and position relative/absolute very judiciously and only where necesary
- 	Doing this will minimize the amount of IE specific code we need

	
##PHP
- Keep your PHP short and free of complex logic
- Break pages up into sub-views and code blocks.
- Use helper functions
- 	if you are repeating ifs
- 	outputing/formatting variables
- use PHP's Alternative syntax for control structures in views
- 	if(/*clause*/): 
- 	/*code*/ 
- 	endif;

##JS
- We use a coding style similar to jQuery's 
- 	http://docs.jquery.com/JQuery_Core_Style_Guidelines
- 	less strict on spacing
- When using JS to create markup, use templating.
- 	We were using trimpath, going forward we will use handlebars.js (http://handlebarsjs.com/)
- keep JS at the bottom of your view if it's short
- For large amounts of JS, put it in an external file.
- boolean variables start with is
- 	var isValid, isOverBudget;
- use === where possible over ==