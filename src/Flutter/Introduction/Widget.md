Describe what their view should look like given their current configuration and state.

When [[State]] changes, the widget rebuilds its description, which the [[Framework]] diffs against the previous description in order to determine the minimal changes needed in the underlying render tree to transition from one state to the next.

Their main job is to implement a [[build()]] function.

Framework builds those widgets in turn until the process bottoms out in widgets that represent the underlying [[Render object]].

Are temporary objects, used to construct a presentation of the application in its current state.

There are some basic widgets:
- [[Text]]
- [[Row]], [[Column]]
- [[Stack]]
- [[Container]]