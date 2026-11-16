# Today, when I tested the yesterday code changes. I found a bug in product form submission that the form is closing before the form is getting submitted.

## I had found the root cause of this bug which is when submit btn is clicked the event is propagating to its ancestor form overlay its event handler is executing the same close product form function.

## But I haven't solved it yet because I need to understand about event propagation when to avoid these type of collissons.

## I raised the issue in the repo and tomorrow I will solve as I'm having exam tomorrow!