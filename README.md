# Op-Amp Based Function Generator

A function generator built purely from op-amps, capable of putting out
sine, square, and triangular waves. Done as part of the **EC Lab** course.

## About the Project

Most function generators you'd buy are built around dedicated ICs, but we
wanted to see if we could get the same three basic waveforms using nothing
but op-amps chained together. It works in three stages:

1. A Wein-bridge oscillator generates the sine wave — this is the only
   place where oscillation actually starts, everything after this is just
   waveshaping.
2. That sine wave feeds a bistable multivibrator (essentially a Schmitt
   trigger), which chops it into a square wave.
3. The square wave then goes through an integrator, which turns it into a
   triangular wave.

We simulated the full chain in LTspice first, then built it on a
breadboard with a couple of potentiometers to tune the frequency, and
checked all three waveforms on an actual oscilloscope to make sure they
matched what we saw in simulation.

Full theory for each stage, the schematic, and both simulated and
hardware waveform captures are in the report PDF in this repo.

## Tools Used

- LTspice
- Breadboard + potentiometers
- Analog oscilloscope
