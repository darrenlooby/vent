
# vent.js

## Hierarchical Eventing System

I wanted to create an eventing system that was a little bit more 'tracable'.

Because of the way I like to organise my event names "fetch stick", and I wanted
my handlers to be as flexible and take away as much of the logic as possible
i.e. be more generic, I wanted to pass through the "caller" of the event too.

I've added a o.seperator so you can just as easily do "fetch/stick" or "fetch:stick"

This makes it very easy to collected "fetch[es]" as it were.
"fetch stick", "fetch ball", "fetch beer" can all trigger "fetch" within the handler.

Equally, "fetch stick", "fetch stick now", and "fetch stick later" - all trigger "fetch" and "fetch stick".

Events are scoped, meaning that you can garbage collect when a window closes if you're eventing from within frames or just want to distroy an entire stack of events.
