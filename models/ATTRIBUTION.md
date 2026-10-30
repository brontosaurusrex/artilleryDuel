# Tank models

## Cocky Tank

`cocky-tank.glb` is the game's original generated tank, edited in Blender for
Cocky Tanks. It includes the custom sloped hull, hollow muzzle, fitted side
armour and curved ribbed mudguards. It is independent of the imported T-55 asset.

## Imported T-55

The T-55 mesh is based on “Tank-T55 toy tank” by EveryThing-Store, CGTrader model 4124545: https://www.cgtrader.com/3d-models/military/military-vehicle/tank-t55-4f536737-2dbc-489f-a684-45df3a5cca05

The listing identifies the asset as Royalty Free. The game uses a geometry-only GLB converted from the OBJ in the supplied `t55-low-poly.zip`. The original texture files and texture references are not included; the game applies its own red and blue materials. The connected turret and gun pieces are separated in the GLB so they can turn and elevate in game.

Rebuild the geometry with Blender using `blender -b --python tools/convert_t55.py -- source.obj public/models/t55.glb`. Only the flat display base is removed. The source millimetres are converted to metres with a rotation that preserves face winding; the hull measures about 6.73 m long and 3.50 m wide. Shared gameplay measurements live in `src/tank-dimensions.ts`.
