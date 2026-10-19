
Experiment Observation:
When _glasses++ was moved outside of setState(), the numbers on the screen did not update when the + button was tapped.

Reason: Flutter needs setState() to know that data has changed. Without putting the changes inside setState(), Flutter will not re-render or update the UI on the screen, even though the number actually changed behind the scenes.