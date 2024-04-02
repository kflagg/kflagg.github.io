---
title: "Maintaining Logical Line Of Inquiry In Data Science"
---


One thing that was constantly reinforced throughout my statistics education
was the importance of starting every analysis from motivating questions with
real-world relevance. These ensure the project maintains direction, leading
to conclusions that are actionable and applicable to the original problem.

It can be tempting to get attached to exciting tools or methods, or to jump to
an untested solution that _seems_ correct, without starting from the beginning
and defining some good questions. This can be an expensive error. I present
two case studies from my career of open-ended data science problems, where
deployable solutions were prematurely promised base on vague questions and a
poor understanding of the data.


## An Unexpected Success

One company with a small analytics team had an occasional but crippling data
quality problem that perpetually annoyed customers, and therefore also the
customer support reps, and in turn the engineers. The software would, at
certain intervals, retrieve the latest chunk of data from a datasource, do
some standardization and augmentation, and then pass along to customers.
Eventually, the customer's data were expected to expire, after which point the
datasource should return nothing. Unfortunately, there were rare but
troublesome and unpredictable situations where, instead of returning nothing,
the datasource would return irrelevant data. I was brought on as a data
scientist, and tasked with solving this.

I was filled in on the background. Everyone agreed that it should be possible
to identify and suppress the irrelevant data. The engineers and analysts had
brainstormed ideas A, B, C, and so on. The ideas varied from simple to
complex, but each one had either performed poorly or no one had had the time
to try it. With my involvement, the idea of predictive models even began to be
tossed around, but it was not clear what might be good predictors. I began by
coding mockups of as many ideas as I could manage, extracting a sample of data
chunks, and assessing. None of the indicators that had been brainstormed did
very well individually. Before continuing on to see if some _combination_ could
be nevertheless useful in a predictive model, I did what should have been the
very first thing done: looked at the data!

I flattened an extract and sorted, keeping data from the same chunks together,
and keeping related chunks next to each other. My eyes immediately saw a very
clear pattern and simple pattern. I coded an indicator for that pattern and
found that it would filter out over 90% of the irrelevant data. I reported
what I had found, an engineer spent less than a day implementing a filter
based on this pattern, and the problem was considered as good as solved. No
predictive model necessary, and I was lauded as a hero.

I actuality, I had simply gotten lucky that there was an easy solution. My
contribution was starting from the beginning: asking "What do we actually know
about the data?" And because the answer was "very little", I looked at some
data.


## A Foreseeable Lack of Success

At another company, one of the data scientists had been experimenting with
[reinforcement learning](https://en.wikipedia.org/wiki/Reinforcement_learning)
(RL) as a hobby side project. This caught on as a buzzword, which led to the
leadership asking, "Could we use this?" "What could we use it for?" "Could we
use it to guide salespersons' actions?" The executives wanted the company to be
seen as a leader in novel AI/ML for practical use, and action recommendation
(AR) also caught on as another buzzword. I was assigned to develop the ARRL,
despite no one having ever asked in which situations (or if at all) the sales
reps needed such a system guiding them.

Leadership wanted a POC of some sort, but this resembled nothing that the
company had ever attempted before, so I got straight to work building the
minimal infrastructure to implement RL. This build itself took several weeks
during which no useful model training and minimal data analysis occurred.

What data analysis did happen was focused on identifying a scenario where the
set of possible actions was small and the state of an account could be
represented very simply. Once I got to any such a case, the problem was so
simple that any sales rep could say exactly what to do. So the benchmark was
to show that RL could perform comparably to a human, and the effort was
justified by training the model with data from accounts worked by experienced
sales staff and using it to help train new hires.

The model persistently produced recommendations that resembled random noise.
But, every so often, my validation runs led to a visualization showing an
interesting enough pattern to keep the leadership hungry. "The model can pick
up real signals! Keep going!" was the attitude.

So I kept going. This had been an order from the top. It never had the baggage
of clear requirements or user stories. Work continued for almost a year, with
the RL model never coming close to being usable.

Some time after leaving this project, I caught up with a colleague who was
still involved with that company. Eventually, they had gone back to the
drawing board to ask "What is an action?" This led to more specific inquiries
about where people actually could benefit from guidance. Ultimately, the grand
all-encompassing RL model idea was abandoned in favor of some small, targeted
enhancements. This took only a matter of weeks.


## The Common Threads

Both of these examples started with a lack of definition. Luck found me a
solution in the first case, and only luck could have provided in the second
case.

In the first example, the reason for the poor definition was simply that no
one had followed the data. I started by understanding the observational units
(chunks) and how those observations change over time. Previous analyses had
either not looked within the chunks, or had flattened and dropped the context
of which data came from which chunk.

The second example was an algorithm in search of an application. There was no
definition in terms of what was needed to be known or done, and any hypotheses
which came up along the way were to be thrown into the RL model. Unfortunately,
the model was just a poor match to the use case, and any line of reasoning
starting from data would have pointed another direction.

Always push back when a data project does not start with questions about data.

