# ppmreader
Arduino class for real-time computation of pulses per minute from some source like a flow meter.

This class does not actually interface directly with the hardware, but is designed to function in conjunction with an interrupt service routine trigged by a pulse from a digital input pin. The class tracks pulses (totalling them) and measures the time between pulses. This is used to compute the current pulses per minute rate at any moment.

To measure flow in some unit of volume per minute, you should fluid through the flow meter and measure it, and then see how many total pulses were counted by the class.  From there you can work out a ratio of pulse per unit of volume.
