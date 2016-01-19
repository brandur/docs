# Engineering

## Organization

### Let a 1,000 flowers bloom.

http://www.gigamonkeys.com/flowers/

* On technical debt:

    > As with financial debt, a small amount, taken on with eyes wide open can be a
    > good thing. But also like financial debt, it compounds over time. A little
    > bit of technical debt taken on when you were ten or a hundred engineers, left
    > on the books, will be killing you when you’re a thousand engineers.

* On technological standardization:

    > During the “let a thousand flowers bloom” phase people will have planted all
    > kinds of exotic blossoms, some of which are lovely and even well adapted to
    > their local micro-climate; you need to be able to decide which ones are going
    > to be first class, nurtured members of your garden and which ones are weeds.

## Server Architecture

http://geocar.sdf1.org/fast-servers.html

* On classic server architecture, and the use of epoll/kqueue vs. libevent:

    > The main loop waits for some event, then dispatches based on the file
    > descriptor and state that the file descriptor is in. At one point it was
    > in vogue to actually fork() so that each file descriptor could be handled
    > by a different thread, but now "worker threads" are usually created that
    > all perform the same task and rely on the kernel to schedule file
    > descriptors to them.
    >
    > A much better design is possible because of the epoll and kqueue, however
    > most people use these "new" system calls using a wrapper like libevent
    > which just encourages the same slow design people have been using for
    > over twenty years now.
