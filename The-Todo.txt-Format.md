h2. Why plain text?

Plain text is software and operating system agnostic. It's searchable, portable, lightweight and easily manipulated. It's unstructured. It works when someone else's web server is down or your Outlook .PST file is corrupt. Since it's been around since the dawn of computing, it's safe to say it's completely future-proof. There's no exporting and importing, no databases or tags or flags or stars or prioritizing or [Insert company name here]-induced rules on what you can and can't do with it.

Todo.txt is a flat text file that contains one task per line, each optionally associated with a context, project and priority for slicing, dicing and sorting.

h2. The 3 axes of an effective todo list

Using special notation in todo.txt, you can create a list that's sliceable by 3 key axes.

*Priority.* Your todo list should be able to tell you what's the next most important thing for you to get done - either by project or by context or overall.

Optionally assign tasks a priority that'll bubble them up to the top of the list.

This is all possible inside todo.txt.

*Project.* The only way to move a big project forward is to tackle a small subtask associated with it. Your todo.txt should be able to list out all the tasks specific to a project.

In order to move along a project like "Cleaning out the garage," my task list should give me the next logical action to take in order to move that project along. "Clean out the garage" isn't a good todo item; but "Call Goodwill to schedule pickup" in the "Clean out garage" project is.

*Context.* _Getting Things Done_ author David Allen suggests splitting up your task lists by context - ie, the place and situation where you'll work on the job. Messages that you need to send go in the "@email" context; calls to be made "@phone", household projects "@home."

That way, when you've got a few minutes in the car with your cell phone, you can easily check your "@phone" tasks and make a call or two while you have the opportunity.

h2. Suggested Todo.txt format

The beauty of todo.txt is that it's completely unstructured; the fields you can attach to each task are only limited by your imagination. To get started, use special notation to indicate task context (like @phone), project (like +GarageSale) and priority (like (A)). So, a todo.txt file might look like this:
<pre>
    (A) @phone thank Mom for the meatballs
    (B) +GarageSale @phone schedule Goodwill pickup
    +GarageSale @home post signs around the neighborhood
    @shopping Eskimo pies
</pre>

A script that perhaps slices out the @@phone@ contextual items and emails them to your mobile phone, for instance, would just output:

<pre>
    (A) @phone thank Mom for the meatballs
    (B) +GarageSale @phone schedule Goodwill pickup
</pre>

A call to @todo.sh@ to just see the garage sale project items would return:

<pre>
    (B) +GarageSale @phone schedule Goodwill pickup
    +GarageSale @home post signs around the neighborhood
</pre>

h2. Other notations

With @todo.sh@, you can choose any unique keyword search by it. For example, to indicate you're waiting on something to complete a task, append the word @WAIT@ to the item in @todo.txt@. Others like to add due dates to a task, @DUE:2006-08-01@. It's completely up to you. To view items by keyword, do @todo.sh list yourkeyword@.