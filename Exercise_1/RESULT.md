## What is happening?
Well, here we see a natural problem when using threads.
There is no ensurance  that the threads will not interfere
with each other. They take the resources, i, whenever they
want, but there is no way to know if the other thread is in
the middle of changing i while this is happening.

The result is as we see, the value of i is not 0 at the end,
but often around 100000 pluss or minus. This is because one
thread will overwrite what the other has written and then use
that value again. It is "ignoring" what the other thread is
doing.
