Uses the [[Context]] to dispatch a convert method. Then uses the [[Block style]] to apply special behavior to blocks of the same family.

Excepting list_item and table_cell contexts, which are not mapped to a handler method and must be accessed from their parent block, there's a 1-to-1 mapping between a [[Context]] and a [[Converter handler method]].