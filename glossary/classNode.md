class node
======

A `class node` is defined as a [node](node.md) within a [concept graph](conceptGraph.md) which tells us something 'interesting' about other nodes, called [class instances](classInstance.md). Typically, the 'something interesting' is something about the format of the class nodes. For example: a class node called `User` might specify that class instance nodes for `Alice` and `Bob` should have a field (under `userData`) called `userName` which should be a string. Formatting information contained within a class node is not necessarily complete; any given node will typically be an instance of multiple class node. 

[DIP-107](../dips/conceptGraph/107.md) provides specification for a [JSON schema](jsonSchema.md) as a particular example of a category of `class nodes`. DCoSL is designed to be flexible, and alternatives to JSON schemas could certainly be utilized as class nodes.

According to the ("class thread rule" ?), a class node is connected to a class instance using a specialized path called a [class thread](classThread.md). The requirement that the class node obeys the formatting rules of the class node is called the (need a name for this?).

In the diagram below, the blue circle is a [class node](classNode.md), the green circles are [class instances](classInstance.md), and each path from the blue circle to a green node is a [class thread](classThread.md).

<img src="../images/concept.png" width="100%" />
