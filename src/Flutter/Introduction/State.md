This objects are persistent between calls to [[build()]], allowing them to remember information.

Change [[Notification]]s flow "up" the [[Widget hierarchy]] by way of [[Callback]]s, while current state flows "down" to the [[Stateless Widget]]s that do presentation. The common parent that redirects this flow is this object.

Subclasses are typically named with leading underscores to indicate that they are private implementation details.

When object is no longer needed, framework calls [[dispose()]].