Bending.ghx  
Bending-Rod.ghx;: Rod  
Catenary.ghx : Load  
Catenary_slide.ghx : LoadVertex  
Catenary2.ghx : LoadVertex  
CirclePacking-OnSurface.ghx  
ClampLength.ghx  
Collision-Balloon.ghx : SolidPointCollide  
Collision-CircleFill.ghx : Collider  
Flag-Wind.ghx : wind sim  
Tensegrity-1.ghx : (Kangaroo1)  
Tensegrity-2.ghx : (Kangaroo1)  

---  

## Kangaroo1  

#### Kangaroo
- KangarooPhysics : Kangaroo Physics Engine v0.099  
  - ForceObject : Collide
  - AnchorPoits  
  - Setting  
  - Geometry ： Geometry to trasform    
  - SimulationReset : toggle

- KangarooSetting : Setting  

#### Forces  
- SpringFromLine : Create Hooke's law springs(フックの法則)  
- unaryForce : Set a vector force / Point, Vector   





---  

## Kangaroo2  

#### Goals  
- Anchor : Set Anchor / AnchorPoint  
- AnchorXYZ : Set AnchorXYZ / AnchorPoint, X(bool), Y(bool), Z(bool)  
- Angle : Set Angle / RestAngle = 最終の角度  
- ClampLength : Keep Length in Range / Line, LowerLimit, UpperLimit  
- Direction :  
- Floor : xy Plane?  
- Length(Line) : Set Length  / Line  
- Load : Set Force Vector / Point, ForceVector  
- OnMesh : Keeping Pt on Mesh / Point, Mesh  
- Pressure : A force normal to each triangle / Mesh, Strength   
- Smooth : Smooth Mesh / Mesh  
- SolidPointCollide : Keep a set of points outside or inside a given Mesh, Collision / pointList, Solid(brep or Mesh), Strength
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
- EdgeLength : Set edge length / Mesh  


---  

## Math  
- Entwine : Flatten and combine a collection of data streams  

## Set  
- CrossReference : 相互参照  

## Display  
- CreateMaterial : OPENGL material, Shader  
  - Kd(Diffuse, 拡散反射光(color))  
  - Ks(Specular, 鏡面反射光(color))  
  - Ke(Emission, 自己発光色(color))  
  - T(Transparency, 透明度(0.0 to 1.0))   
  - S(Shine, 光沢(0 to 100))  
