

	#Allow Flexbox display
		display: flex;

	#Align items horizontally
		justify-content:
			#Options include:
				flex-start; - items align to left of container
				flex-end; - items align to right of container
				center; - items align at center of container
				space-between; - equal spacing between items, with first at start and final at end
				space-around; - equal spacing around items
				space-evenly; - even spacing around items with a full space at either end

	#Align items vertically
		align-items:
			#Options include:
				flex-start; - items align to top of container
				flex-end; - items align to bottom of container
				center; - items align to vertical center of container
				baseline; - items align to baseline of container
				stretch; - items stretched to fit

	#Change direction
		flex-direction:
			#Options include:
				row; - items placed the same as text direction
				row-reverse; - items placed opposite to text direction
				column; - items are placed top to bottom
				column-reverse: items are placed bottom to top

	#Align specific item
		align-self:
			#Options include same values as 'align-items' but for a specific item
			#Overrides 'align-items'

	#Wrap items
		flex-wrap:
			#Options include:
				nowrap: every items is fit to a single line
				wrap: items wrap around to additional lines
				wrap-reverse: items wrap around to additional lines in reverse

	#Combination of direction and wrap
		flex-flow:
			#Options include:
				row wrap; - sets rows and wraps them
				row nowrap;
				row reverse nowrap;
				column reverse;
				column wrap-reverse
				column wrap

	#Space multiple lines a certain way
		align-content:
			#Options include:
				flex-start; - lines packed at top of container
				flex-end; - lines packed at bottom of container
				center; lines packed at vertical center of container
				space-between: lines display with equal spacing between them
				space-around: lines display with equal spacing around them
				stretch: lines are stretched to fit the container

	#Order items
		order:
			#Can be positive or negative. Default order value of 0.
