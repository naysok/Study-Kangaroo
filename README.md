Sample Files  

Bending.ghx  
Bending-Rod.ghx : Rod  
Boxes-Mechanism.ghx : RigidBody  
Catenary.ghx : Load  
Catenary_slide.ghx : LoadVertex  
Catenary2.ghx : LoadVertex  
CirclePacking-OnSurface.ghx : Load,   
ClampLength.ghx  
Collision-Balloon.ghx : SolidPointCollide, Pressure, Floor  
Collision-CircleFill.ghx : Collider  
Collision-Cloth-inflatable.ghx : SphereCollide, Floor, Volume, CombineAndClean  
Collision-Curve-X-Particle-2d.ghx : curvePointCollide, Load  
Curve-to-Balloon.ghx : MeshMachine, Peressure, Anchor  
Flag-Wind.ghx : wind sim  
Inflation.ghx : Pressure,LineLength, 膨らむ  
Man.ghx : 身体リグ  
Mechanical-Assembly.ghx : AlignFaces, Concentric  
MeshMachine-01.ghx : MeshMachine, removeDuplicatePts, Sequence  
MeshMap-Morphing.ghx : MeshMap  
Kangaroo1-vs-Kangaroo2.ghx : MeshCourners, SpringFromLine, unaryForce, StepSolover  
Polygon-MagnetSnap.ghx : MagnetSnap  
RigidBody-Balance.jpg : RigitBody, SolidPlaneCollide  
Simple-Tent-JH.ghx : load, anchor, length   
Strand-Beest.ghx : Trail, counter  
Tensegrity-1.ghx : (Kangaroo1)  
Tensegrity-2.ghx : (Kangaroo1)  


---  

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
- Sequence : Connect to the Reset input to output a time sequence of the simulation / Frame  
- counter : Connect a Timer to this and it increments by 1 with every update, + Timer  


#### Forces  
- SpringFromLine : Create Hooke's law springs(フックの法則)  
- unaryForce : Set a vector force / Point, Vector  


####  Utility  
- MeshCourners : Finds the corners of the boundary of a mesh  
- Trail : Draw a trail of a point's motion (trail 軌跡) / Point, Record(bool)  




#### Mesh  
- CombineAndClean : Combine and Clean a list of meshes, removing unused and duplicate  
- MeshMachine : Remeshing tool  
  - Geom (input geometry surf or mesh)  
  - FixV (Points to keep fixed during remeshing 外形など)  
  - Reset (Sequence = 10??)  
- MeshMap :  Morphing / M1(SourceMesh), M2(TargetMesh), P(Vertices of mesh to transform)  




---  

---  


## Kangaroo2  


#### Goals  
- Anchor : Set Anchor / AnchorPoint  
- AnchorXYZ : Set AnchorXYZ / AnchorPoint, X(bool), Y(bool), Z(bool)  
- Angle : Set Angle / RestAngle = 最終の角度  
- ClampLength : Keep Length in Range / Line, LowerLimit, UpperLimit  
- Collider : Collisions between thickened line segments and spheres  
- CurvePointCollide : Keep a set of points outside or inside a given 2d curve  
- Direction :  
- Floor : xy Plane?  
- Length(Line) : Set Length  / Line  
- Load : Set Force Vector / Point, ForceVector  
- MagnetSnap : Snap Points togetther according to proximity / Points, Renge(snapable length)  
- OnMesh : Keeping Pt on Mesh / Point, Mesh  
- OnPlane : Keep a point on a given plane / Point, Plane  
- Pressure : A force normal to each triangle / Mesh, Strength  
- RigidBody : RigidBody / Part(Mesh)  
- Smooth : Smooth Mesh / Mesh, RB(output)  
- SolidPointCollide : Keep a set of points outside or inside a given Mesh, Collision / pointList, Solid(brep or Mesh), Strength  
- SphereCollide : Collisions between large numbers of equal sized spheres / Point, Radius  


#### Main  
- Grab : ?  
- Solver : Goal をまとめて計算  / GoalObjects  
- Solver(bouncy) : Solver with momentum(弾力、弾み) / GoalObjects  
- StepSolover : アニメーション?  
- Show : Show  


#### ?  
- AlignFaces : align faces of a pair of rigid body  
- Rod : Resistant rod, Angle に似てる  
- LoadVertex : Load に近い / Mesh, Strength(上or下)  
- EdgeLength : Set edge length / Mesh  
- Volume : set volume  
- Wind : Setting Wind / Mesh, WindVector  
- CombineAndClean : Combine and Clean a list of meshes, removing unused and duplicate  
- removeDuplicatePts : Removes Similar points from a list / P(List of points to clean)  
- Concentric : align axis of a pair of rigid body  
- SolidPlaneCollide : Collision between a plane and a solid  






---  

---  


## Grasshopper Components  


#### Math  
- Entwine : Flatten and combine a collection of data streams  
- Weave : Weave a set of input data using a custom pattern / P(pattern), data1, data2  


#### Mesh  
 - Mesh WeldVertices : merge identical vertices, 同じ頂点をマージ(weld 溶接)  


#### Vector  
- Closest Point : Find closest point in a point collection /P(Point), C(Cloud Point to search)  
- Closest Points : Find closest points in a point collection / P(Point), C(Cloud Point to search),T   


#### Set  
- Clean Tree : remove all "null" and invalid items from a data tree / T(DataTree)  
- CrossReference : 相互参照  
- Cull Index : cull(remove) indexed elements from a list  



#### Display  
- CreateMaterial : OPENGL material, Shader  
  - Kd(Diffuse, 拡散反射光(color))  
  - Ks(Specular, 鏡面反射光(color))  
  - Ke(Emission, 自己発光色(color))  
  - T(Transparency, 透明度(0.0 to 1.0))   
  - S(Shine, 光沢(0 to 100))  
