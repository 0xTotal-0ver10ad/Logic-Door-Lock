Digital Logic Door Lock System (on protous)
A hardware-based security system designed using discrete logic gates and counters. This system compares a user-defined password against a preset code to control a locking mechanism.

System Overview
The circuit uses a combination of logic gates for password verification, a flip-flop for state management, and a counter with a 7-segment display to track attempts or system status.

Components Used
Logic Comparison: XNOR Gates (4077) and AND Gates (U2, U3, U4) to compare the 4-bit switch inputs.

Input: Two sets of DIP switches (DSW1 and DSW2).

Memory/State: D-Type Flip-Flop (U5) to hold the lock/unlock state.

Indicators: * Green LED (D1): Access Granted / Unlocked.

Red LED (D2): Access Denied / Locked.

Display System: * 74193 4-Bit Binary Counter.

7448 BCD-to-7-Segment Decoder.

Common Cathode 7-Segment Display.

Clock/Control: Manual push button and logic NOT/AND gates for pulse management.

How it Works
Password Entry: The user sets a 4-bit code using the DIP switches.

Logic Verification: The XNOR gates compare each bit of the two switches. If all four bits match, the final AND gate (U4) sends a HIGH signal.

Lock Trigger: When the button is pressed, the D-Flip-Flop captures the result of the logic comparison.

Output: * If the code is correct, the Green LED turns on.

If the code is incorrect, the Red LED turns on.

Counter: The system is wired to a counter and 7-segment display, which can be configured to count successful entries or failed attempts based on the clock pulses from the logic gates.
