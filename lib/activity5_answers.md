Experiment Observation:
When the button corner radius was changed from 8 to 20 inside buildTheme(), the corners of the ElevatedButton became significantly more rounded.
Reason: Updating the value in buildTheme() applies the new shape style globally to all ElevatedButton widgets across the entire app that rely on the central theme.