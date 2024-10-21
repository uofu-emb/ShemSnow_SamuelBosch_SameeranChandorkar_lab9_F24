In this lab, we:
 - Read a problem
 - Wrote a Finite State Machine for the problem
 - Filled out a state transition table for the problem that was pre-filled for us
 - Wrote another Finite State Machine based on the completed table.

The problem we solved was a Railrod crossing problem:

Implement a FSM for a safety warning system to prevent crossings while a train is approaching and until it has passed.

There are two tracks, one going north and the other south. Trains on each track only run in one direction.
The tracks meet at a crossing. [Oct 16: this interpretation is allowed but not preferred] At the crossing, a roadway (for cars, pedestrians, baby strollers, etc.) intersects both tracks. See "diagram.png" for clarification.
Each track has two proximity sensors approach and depart, placed on the tracks before and after the crossing respectively.
The two approach sensors emit the events northbound_approach and southbound_approach when the first car of the train crosses the sensor (leading edge).
The two depart sensors emit the events northbound_depart and southbound_depart when the last car of the train crosses the sensor (trailing edge).
The system has an audible alarm, which can be in the state on or off, and a barrier that is in either lowered or raised state to block the crossing.
A timer emits an event elasped 10 seconds after the alarm starts ringing.
When a train is approaching:
The alarm begins clanging.
After 10 seconds, the barrier lowers.
The alarm continues to sound and the barrier remains lowered while a train is present.
When no train is present the barrier raises.
After 10 seconds the alarm stops.


Our list of invariants is inside the excel spreadsheet.