# Acquire core logger

Acquire reports debug and trace events by printing them through a "logger".
This library defines what that is and provides a function for setting a global
callback at runtime that handles incoming messages.

This involves very little code. It barely merits being its own library. It's
here to define what the expected callback interface is - something almost every
component needs to know about.
