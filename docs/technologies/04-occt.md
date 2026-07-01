# OCCT

OCCT is the industrial geometry kernel in the leverage model. It already provides BREP, STEP, IGES, topology, meshing, and geometry algorithms at a level EngineeringOS should not attempt to recreate.

## How EngineeringOS Uses It

EngineeringOS should use OCCT as a geometry backend for mechanical and 3D-adjacent capabilities, typically through dedicated plugins or integration layers rather than by absorbing the kernel into the platform core.

## Boundary

The rule from the draft is strict: never rewrite the geometry kernel. EngineeringOS should integrate OCCT, not compete with it.
