# ElhexDelivery

An Elixir OTP application that demonstrates some GenServer uses.  This code is part of a video
tutorial series.

* [Part 1](https://youtu.be/EDu3EwTbrFM)
* [Part 2](https://youtu.be/rMwEQZewDyk)

The tests all pass when run under Linux, but eight fail under Windows -- all eight failrues seem to relate to the line endings in the data file.  FWIW. it seems that this hiccup could be curried.   
. . . investigating . . . .

Solved by replacing Unix specific implementation split at line ending with generic handler -- String.split(~r/\R/)
