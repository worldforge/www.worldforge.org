---
title: "Out-of-process mind code"
date: 2015-05-27
---

{{< imgresize "img.png" "360x360" "Edit minds" "float:left; padding: 5px;">}}
I just pushed a rather large changeset to the Cyphesis server which redesigns the mind code so that all AI code now is handled by one or many processes separate from the server.

This is a big change to how the Cyphesis server works. Previously all world simulation and mind code was handled by the one Cyphesis executable, in one single threaded process. Now the server instead only focuses on world simulation and various house keeping tasks, while separate processes handle all AI code.

There's a new executable, "cyaiclient", which when invoked will use a local socket to connect to the server and act as an AI client. Many such clients can be run in parallell, each one handling one or many minds.

The advantages to this are manifold.

*   It lets us better take advantage of multicore system (which is the norm since a couple of years) without having to rewrite the single threaded nature of the Cyphesis server. Each AI client is single threaded, but multiple clients can run in parallell.
*   It makes the server less complex, since AI execution is handled separately. This makes it easier to reason about and work with.
*   It allows for an improved workflow when developing AI code. The AI code can now be altered and restarted without the server being touched. This allows for more a more efficient iterable approach.
*   More avenues for alternative AI clients are now open. The current AI code uses mainly Python. It's now much easier to implement an AI client in a separate language (Prolog anyone?).
*   The door is now open for letting AI clients run on separate machines. Say, in a cloud. While the current code requires the AI client to connect using a local socket, implementing support for remote connections should be trivial.

When Cyphesis now is run it will by default spawn a child AI process. This behaviour can be tuned through the "--cyphesis:aiclients" flag. Setting it to zero, as such "--cyphesis:aiclients=0" will disable the automatic client spawning, thus allowing you to run your own client process. This is useful when developing.