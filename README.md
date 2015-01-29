
# Priority Queue Data Structure

## Description

This is a javascript implementation of a
[priority queue](http://en.wikipedia.org/wiki/Priority_queue)
data structure.

A simple queue data structure models the notion of 'First in First Out', or
FIFO&mdash; image the line at the grocery store.  The first item to be removed
from a queue is the first item placed in the queue.  Basically, the order in
which items are placed in the queue is the only factor that determines thier
placement; there is no notion of 'priority'.

A priority queue differs from a simple queue in the way the items are added to
the queue.  Each item in a priority queue has a 'priority' associated with it
that determines where in the queue it is to be inserted.  Items with a 'higher
priority' are inserted ahead of those that have a 'lower priority'.  Items with
the same priority are inserted in the order they are added.

This particular implementation utilizes a
[linked list](https://www.npmjs.com/package/dbly-linked-list) as the
underlying data structure.  This offers several benefits.

* We can leverage the work that has already been done to implement the
  linked list.

* This lends itself to a level of composition and abstraction which greatly
  simplifies this implementation.  It provides a wrapper around only those
  methods of the linked list that we need to construct the properties of a
  queue data structure.

* The 'queue' or 'dequeue' operations can be completed in O(1) time.

* No additional overhead is required to 'resize' the data structure to add
  more elements to the queue.  When elements are 'queued' up in the queue, the
  underlying linked list will adjust its size dynamically.

*For specific examples and documentation, see the below sections*

### Motivation:

The main purpose of this project is revisit the basics, and focus on the
development process.

*I wholehearedly acknowledge that the basic data structure space is populated
with well-written code and efficient implementations, and one could easily grab
one of those libraries and integrate it in their project.  However, the main
difference between those libraries/implementations and this one is that this is
the best implementation I have ever written.  My hope is that someone else will
find this useful, but understand, this code is not the goal; this will simply
be a useful bi-product of the journey.  The underlying motivation is to
understand and, more importantly, learn from the process to get to the desired
end-state&mdash;for me it is all about the joy of the journey.*

#### Environment:

Although this implementation is designed to be used with
[Node.js](http://www.nodejs.org), it could be used in other contexts with minor
modifications.  This implementation does not have any external dependencies
that would preclude it from being used in the browser--just include it with a
`<script>` tag and it should be good to go.  _Disclaimer: I have not tested
this implementation in any other context/environment; only tested with node.js_

----