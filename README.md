# How to Design an Unmaintainable Architecture

It's been a while since Roedy Green's classical [How To Write Unmaintainable Code](https://www.mindprod.com/jgloss/unmain.html).
The software world has changed. A software project nowadays consist not only of code, but also of cloud-allocated resources,
deployment scripts, build pipelines, security policies, API configurations - A whole new world of mission-critical details.
Some of these facilities not only help run your application, but also protect it from errors and glitches, 
making programs *easier* to maintain! Therefore, as a software architect, your job security depends not only on preventing any
maintenance programmer from changing your code, but also making sure none of those code pups could ever update your deployment plan.

As a service to the community, we offer this compiled collection of obfuscation techniques, so that our fellow senior developers could
maintain their exagguratedly high-paying jobs forever. Feel free to contribute by sending a Pull Request!

## Disclaimer
This article is a **joke**. It aims as pointing out bad practices by rediciuling them. 
DO NOT try these techniques in the wild! They will lead only to sorrow and destruction.

## Architecture diagrams
Your job as an architect is not to cater for all of those pesky details. It is **to lead**. To point out the way.
You are no longer a developer. You are a visionary; an entrepreneur, just without the financial risk (or benefit).
Therefore, you cannot be expected to actually *write code* that implements your vision. This is for lesser men.
Your job is present the one-and-only ideal solution to both management and co-workers, and let them take it on from there - 
and no presentation is ever complete without a diagram.

### Keep it simple
Visual hints, such as shapes and colors, are more a distraction than help. There is no need to use one of those carefully-designed
icons sets of cloud services, or, *shudder*, a formal graphical notation. Instead, go with a classic block diagram, made of those 
wide-margin, small-font boxes, connected by half-point arrows. If you must use colors, stick to PowerPoint's default pallate of
high-saturation colors that poke viewes' eyes and hide away black letters. 
If it is good enough for an elementary school multimedia class, it's good enough for the board of directors!

- [ ] Add monochrome diagram example
- [ ] Add diagram example with really ugly colors

### The big picture
The human visual cortex can process between 5 and 9 graphical elements in a single glance. This is why diagrams are so useful.
It also means that anything beyond those few elemenets is distracting. Therefore, keep your diagram to a handful of top-level
components. If you have just "client", "data" and "business logic", you probably got all your bases covered.
Also, add an "AI" box and don't connect it to any of the other ones. It will confuse your engineers, but make investers happy.

### Form follows function
Do not specify what type of cloud resource should be set up in place of which shape in your diagram. 
Do not use familiar icons, or write the specific resource type. Instead, describe the *function* of each component,
like "storage" or "processing".
If your team can't tell if "users preference store" should be an expensive on-demand transactional database, 
or a bunch of files on an S3 bucket, they have no business implementing it.
Likewise, keep them guessing if the "process" node should be a time-limited lambda function, or a 100-nodes strong Apache Spark
cluster for a 3-days batch. It will keep them on their toes.

### Time flies like an arrow, fruit flies like a banana
Mix more than one kind of relations into one diagram, using the same kind of arrows. 
For example, make a connector means either "function invocation" or "development dependency". Mix the kinds sporadically.
