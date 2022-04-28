# Demultiplexer
**A circuit that forwards an input to one of several outputs.**

A demultiplexer or *demux* is the inverse of a [[multiplexer]]. For $2^n$ output lines, a demultiplexer is controlled by $n$ *control* lines.

A demultiplexer is essentially a [[decoder]] with an enable line. Below is a $1$-to-$4$-line demultiplexer contructed using a $2$-to-$4$-line decoder and AND gates.

![[DemultiplexerConstruction.svg]]