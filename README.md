# Maydef #

Why Maydef? Because I use it to defend my sectors in Mayhem. Don't really
have that much use of it in normal LU. Maybe someone has a better idea for
a name.

## What? ##

This is a script for MLCC in Litcube's Universe (will not work for
normal AP). You enable it through a hotkey to run on a dock and it
will send MLCC ships to sectors where you have stations that have
baddies in them.

## How? ##

Assign hotkey for "Mayhem defense". Push hotkey. Click on "Defense
dock", click on pretty much any station, but I'd recommend an MLCC
dock (I might fix things in the future so that you can only use MLCC
docks for this). That's it. Now your MLCC ships will fly out to shoot
baddies in your sectors.

## UI ##

On top of every menu there is the name of the station where the script
is running. If new defense missions are blocked it will be indicated
after the name. Below is a line for blocking all new defense missions
and making all defense ships retreat. You might want to use that
before taking command of MLCC ships yourself (although we will not try
to use ships that aren't currently docked).

The first menu is "Sectors". This contains a list of the sectors we
care about (sectors where you own stations), current threat value of
the enemy ships in the sector and current threat value of the ships we
sent there to defend. Below, we have a list of extra sectors we guard
and a selection to add more sectors to this list.

The second menu is "Options". "Enemy:defender threat ratio" is how
much overkill we want to use on the enemy ships. `1:2` means that for
each enemy M6 we send two of our M6s (or equivalent fire power).
"Block defenders" does what it says. Below you can set here how
threatening you think various ship classes are. This is applied
equally to enemy and your own ships. Your own carriers also count
their docked fighters into their threat. We don't do that for enemy
carriers (but when the enemy carrier launches fighters, we'll notice
that and send reinforcements if necessary).

The third menu is "Log". This contains a bunch of spam about various
decisions that we make and hopefully no error messages.

## Misc and bugs ##

Below are a few notes on how things behave and a few problems that I
might fix if there are any users.

### Why is it run on a dock? ###

You designate a dock to be your military headquarters and that dock
has a staff that monitors satellites and I don't know what more to say
here because I suck at roleplay. The actual reason is that I haven't
bothered figuring out how to run and manage scripts that run somewhere
that isn't stations or ships. It might be possible, but why not?

But what happens if the dock gets destroyed you ask? Well, you'll have
to push a few buttons again.

### How do we decide which ships to send? ###

Any ship in MLCC with intercept enabled is up for grabs.

The ships are sent first come, first serve. We don't try to match
smallest possible ships to send. Yes, we might end up sending an M2 to
swat an M5 fly. Yes, this should probably be improved.

In the worst case, just do a normal MLCC retreat. This will make the
defense ships go home and if the threat is still there we'll send in
the next ship in line.

### What orders do ships execute? ###

The ships behave just as if you have pressed the assist button and
then the go button in normal MLCC. Except that the last order is always
'Retreat'.

### Why do ships jump in to some gate far away from the enemy? ###

Because they either jump to the center of the sector if you haev QJE
or its nearest gate if you don't. It's pretty useless to jump to the
nearest gate to the enemy because pretty much by definition they'll be
heading away from it. If the enemy is fast enough the defender ships
won't ever catch up. At some point in time we might want to figure out
where the enemies are heading. Unless there are multiple groups of
them.

### Help, my whole fleet is chasing an M5. ###

We don't withdraw ships once the threat goes down. We probably should,
but there are risks with doing that (like if the threat drops because
a carrier docks its fighters and then relaunches those fighters we
could end up oscilating).