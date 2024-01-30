---
tags:
  - interactable
  - "#WIP"
---
# _Grind Rail_

Type: [[Interactables]]

----


[[Player]] follows [[Path2D]] using the [[Grind]] ability

#WIP [[Interaction]] with [[grapple hook]] would be cool, like hanging down from it

As a quick addendum to the resources above in case anyone winds up here with the same question as me:

- The Path2D node is the parent, and in the UI you can set points that make up the path (this will be built as a Curve2D object which you can see in the Inspector)
    
- You add a child to the Path2D node, the PathFollow2D node
    
- The PathFollow2D properties are offset (distance from the first point to the last point in absolute numbers) or unit_offset (distance from first point to last point between 0 and 1)
    
- If you wanted a player controlled character to walk along it, you would do the following:
    
    - Attach the Player Node (whatever it is) as a child to PathFollow2D
        
    - Have the input change the offset or unit_offset property of PathFollow2D (for example, left would reduce it and right would increase it).
        
    - If you turn Loop (another property in PathFollow2D) off, then there will be terminal points at the left and right.


## Similar in other games
* [[Convergence LoL]]
* [[Sonic]]

