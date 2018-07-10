## This is a Composite Chart lesson (from Code Institute Full-Stack Diploma course). Transcription from lessons, included in comments sections in the code.

# COMPOSITE CHART.

- What is it?

Composite Chart. 


- What does it do?

It is a chart of the relationship between the groups within a dimension.


- How do you use it?

Use a composite chart to view and compare groupings within a dimension.


Firstly Create directory - mkdir data
Change directory - cd data
Input on command line to quickly retrieve raw json data - wget https://raw.githubusercontent.com/Code-Institute-Solutions/DataVisualisation/master/data/transactions.json.

LESSON:
In our last example we tracked the total spend over a particular time period
actually over the entire time period available to us from our data set. But
what if we wanted to view Tom's spend over that time period or
Alice's spend or Bob's spend over that time period? One way of doing it would be
to create an individual graph for each. But a more efficient way of doing that
could be to create a composite graph or a composite chart where we can see Bob's
Alice's and Tom's spent all in the same chart. We can easily make a visual
comparison between the spends. So let's do that now. We have the basics of our
functions in place - that's often called boilerplate in software development.
So we have our makeGraphs() function in place. We have our Queue() with our imports.
We have already parsed the data copy and paste they the formatting functionality
and let's get our date dimension
and group it and reduce to the spend
in this case we're going to do a check we're going to say if the name is equal
to Tom then we're going to get the spend
that instance that spend instance for Tom and you might notice there the plus
in front of the D well that's a JavaScript shortcut our little trick
that converts attempts to convert a number that's been represented in string
format into an actual number so that's Tom spend by month it's a way of
cleaning up the data as well it's a way of avoiding dirty data so if if we can't
convert the string the spend string to an integer we return zero instead and it
allows us to render our charts more easily so we have Tom Bob and Alice
so if Tom spend by month Bob's spend by months and Alice spend by month then we
create our composite chart
once we have created the composite chart object we then begin the process of
chaining our functions so we can provide attribute values so we give it a height
and a width height of 990 a width of 200 and our dimension that's the data
dimension that we're going to work with number again we're going to use a time
scale as opposed to a linear scale or an ordinal scale and we use our min data
and Max data to provide our domain give our y-axis a label and we call it spend
we're introducing a legend here as well and our positioning of the legend to
remember that's the positioning relative to the chart itself within the viewport
and there's a gap of five units there will be a color-coded legend for Tom Bob
and Alice and we're also rendering our horizontal gridlines again to provide
more visual cues when comparing and contrasting then we invoke the compose
function and inside there where we create a line chart
so we then group
and do we repeat so we create one for for Tom we create a line chart for Bob
and we will create a line chart for Alice
we set the brush on to false remember in the last unit that brush we mentioned
that the brush is on by default you can specify brush on to be false
remember called render all unless you call render all the chart won't render
it won't display on your browser
there you go that's pretty nice again it's interactively click on the legend
those individual spends will be highlighted so let's refactor a little
bit you can see that where we have Tom spent by month Bob spent by month on a
less bandwidth and the code looks almost identical except for the string name
that we're matching so we can be a bit more clever about more efficient or what
I call lazy good programmers are lazy programmers and when I say lazy I mean
efficient why reinvent the wheel why repeat yourself if you have the
opportunity to create a piece of code once and just pass different parameter
values then that's more efficient reduces file size as well we created a
function called spent by name that takes in a string let go that's called name
and that's with all variables name your parameters in such a way that reflects
the data being passed in so we're expecting names so we call it name
this allows us to reduce our file size and make our code that little bit more
readable
okay still works there you have it a composite chart
