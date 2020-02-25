# Encoders
LPD3806 optical encoder
It is a cheap optical encoder from China. They suffer from many compromises that degrade serious results.

- supply voltage is recommended 5-24V - it is wrong. Encoder contains a classic linear stabilizer 7805, which needs for its proper operation at least 7.5V. When powering 5V encoder works poorly (electronics gets instead of 5V only about 2.5V), losing pulses.
- with 12-24V power supply there is another problem with heat dissipation at 7805

- Another problem is the transmission of the quadrature signal. The encoder is connected as an open collector. Although the cable is shielded, but if it leads around the induction power supply (switched power supplies, stepper motor, ...) the signal is very susceptible to interference.

After reworking:
- output reworked to DIFFERENTIAL LINE DRIVER
- supply voltage is only 5V, no protection !!!
- added non-inverting Schmitt trigger

To rework your encoder, you will need to carefully disassemble it and most components will be reused.

Tools:
- screwdriver
- table solder
- heat gun
- tweezers
- good luck
