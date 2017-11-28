Bending.ghx
Bending-Rod.ghx;: Rod
Catenary.ghx
Catenary_slide.ghx
CirclePacking-OnSurface.ghx
ClampLength.ghx
Flag-Wind.ghx : wind sim

---

## Kangaroo1


---

## Kangaroo2

#### Goals
- Anchor : Set Anchor / AnchorPoint
- AnchorXYZ : Set AnchorXYZ / AnchorPoint, X(bool), Y(bool), Z(bool)
- Angle : Set Angle / RestAngle = 最終の角度
- ClampLength : Keep Length in Range / Line, LowerLimit, UpperLimit
- Direction :
- Length(Line) : Set Length  / Line
- Load : Set Force Vector / Point, ForceVector
- OnMesh : Keeping Pt on Mesh / Point, Mesh
- Smooth : Smooth Mesh / Mesh
- SphereCollide : Collisions between large numbers of equal sized spheres / Point, Radius


#### Main
- Grab : ?
- Solver : Goal をまとめて計算  / GoalObjects
- Solver(bouncy) : Solver with momentum(弾力、弾み) / GoalObjects
- Show : Show

#### ?
- Wind : Setting Wind / Mesh, WindVector
- Rod : Resistant rod, Angle に似てる
- LoadVertex : Load に近い / Mesh, Strength(上or下)
-
