**[ Sample Files ]**  

[https://github.com/Dan-Piker/Kangaroo-examples](https://github.com/Dan-Piker/Kangaroo-examples)  



Beam-Analysis.gh : Beam, Support, C#  
Bending.ghx  
Bending-GridShell.ghx : Angle, Load, OnCurve  
Bending-Mesh-Angle.jpg : Angle, LineLength    
Bending-Rod.ghx : Rod  
Bomb.ghx : Bomb, SolidPlaneCollide, load, Floor, Anchor,  
Boxes-Mechanism.ghx : RigidBody  
Catenary-1.ghx : Load  
Catenary-2.ghx : LoadVertex  
Catenary-Galapagos.ghx : ZombieSlover, Garapagos
Catenary-slide.ghx : LoadVertex  
CirclePacking-Fill.ghx : c#, OnMesh, Collider  
CirclePacking-Image.ghx : ImageCircle  
CirclePacking-OnSurface.ghx : Show, OnMesh, SphereCollide  
CirclePacking-OnSurface-Pull.ghx : Show, OnMesh, SphereCollide, Anchor  
ClampLength.ghx  
Collision-Multi-Radius-Spheres.ghx : Collider  
Collision-Multi-Radius-Spheres-Lines.ghx : Collider, LineLength  
Collidion-Rigid-Mesh-X3.ghx : X2,X3,X4, SolidPlaneCollide, Load, RigitBody, SolidCollide  
Collidion-Rigid-Mesh-X10.ghx : X10,X28, SolidPlaneCollide, Load, RigitBody, SolidCollide  
Collidion-Rigid-Solid.ghx : X16, SolidPlaneCollide, Load, RigitBody, SolidCollide  
Collision-2D-Shapes.ghx : Collide2d, PolygonArea, OnPlane, LineLength  
Collision-Balloon.ghx : SolidPointCollide, Pressure, Floor  
Collision-Cable.ghx : LineLength, Collider  
Collision-Chain.ghx : RigidPointSet, Collider  
Collision-Cloth-Drape-XXX.ghx : SolidPointCollide, load, Smooth, Floor, LineLength  
Collision-Cloth-inflatable.ghx : SphereCollide, Floor, Volume, CombineAndClean  
Collision-Cloth-Grabe.ghx : EdgeLength, SphereCollide  
Collision-Curve-X-Particle-2d.ghx : curvePointCollide, Load  
Collision-Floor.ghx : SphereCollide, Floor, load  
Collision-Simple.ghx : ClampLength  
Collision-Solid-X-Particle.ghx : SolidPointCollide, SphereCollide, Load  
Curve-to-Balloon.ghx : MeshMachine, Peressure, Anchor  
Custom-Goal-1.ghx : c#  
Custom-Goal-2.ghx : c#  
Custom-Goal-PointCreation.ghx : c#, SurfaceClosetPoint  
Custom-GoalDebugger.ghx : c#  
Custom-GrowingLine.ghx : c#  
Custom-Solver.ghx : c#  
Custom-Solver-StepByStep.ghx : c#, NakedVertices  
Custom-Solver-Tensile-Relax.ghx : c#  
Directional-Stiffness.ghx : Hinge, SolidPointCollide  
Drape-Grid.ghx : Load, SolidPointCollide, Floor  
Flag-Wind.ghx : wind sim  
G2-Curve.ghx : CoPlaner, G2, Coincident  
Inflation.ghx : Pressure,LineLength, 膨らむ  
Man.ghx : 身体リグ  
Mechanical-Assembly.ghx : AlignFaces, Concentric  
Mesh-Shell-Hinge.ghx : HingePoint, Hinge  
MeshMachine-01.ghx : MeshMachine, removeDuplicatePts, Sequence  
MeshMap-Morphing.ghx : MeshMap  
Kangaroo1-vs-Kangaroo2.ghx : MeshCourners, SpringFromLine, unaryForce, StepSolover  
Origami-1.ghx : Hinge, LineLength, Anchor  
Origami-2.ghx : Hinge, LineLength, Anchor, Planarize  
Origami-3.ghx : HingePoint, LineLength, Anchor, Planarize    
Polygon-MagnetSnap.ghx : MagnetSnap  
Raisin.ghx : Volume, Smooth, SphereCollide, Average, LineLength しぼむ  
RigidBody-Balance.jpg : RigitBody, SolidPlaneCollide  
Set-Lengths-Random.ghx : LineLength  
Simple-Tent-JH.ghx : load, anchor, length   
Strand-Beest.ghx : Trail, counter  
SplitAtCorners. ghx : SplitAtCorners, MeshCourners, Discontinuity  
Tensegrity-1.ghx : (Kangaroo1)  
Tensegrity-2.ghx : (Kangaroo1)  
Tensile-Cone.ghx : Refine, OnCruve, LineLength, CombineAndClean  
Tensile-Diagonalize.ghx : Diagonalize, LineLength, Anchor  
Tensile-Ridge-Beam.ghx : Anchor, Length, OnCurve  
Tensile-Ridge-Cable.ghx : Anchor, LineLength  
Tensile-Simple.ghx : Anchor, EdgeLength  
Tensile-SoapFilm.ghx : SoapFilm, TangentialSmooth, Anchor, NakedVertices  
Tensile-Tunnels.ghx : Refine, OnCurve, LineLength  
Tensile-Tunnels-WarpWeft.ghx : WrapWeft, Refine, OnCurve, LineLength  



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
- NakedVertices : 端点を探す？, Anchor に : Mesh(input)  
- Refine : Divide each quad into 4 quad, and each triangle into 4 triangle / Mesh, Level(Level of Subdivision)  




---  

---  


## Kangaroo2  


#### Goals  
- Anchor : Set Anchor / AnchorPoint, TargetPoint(The 'P' input of the Anchor identifies which points to move, and the 'T' input tells it where to move them to.)  
- AnchorXYZ : Set AnchorXYZ / AnchorPoint, X(bool), Y(bool), Z(bool)  
- Angle : Set Angle / RestAngle = 最終の角度  
- ClampLength : Keep Length in Range / Line, LowerLimit, UpperLimit  
- Coincident : Equivalent to a zero length constraint between a pair of points / Point1, Point2  
- Collide2d : Collisions between closed polygons in a given plane / polyline  
- Collider : Collisions between thickened line segments and spheres / Objects, Radius(Multi-Radius OK?, SphereCollide 違う)  
- CoPlanar : ?  
- CurvePointCollide : Keep a set of points outside or inside a given 2d curve  
- Direction :  
- Floor : xy Plane?  
- Length(Line) : Set Length  / Line  
- Load : Set Force Vector / Point(DeconstructMesh の V とか), ForceVector  
- MagnetSnap : Snap Points togetther according to proximity / Points, Renge(snapable length)  
- OnCurve : Keep a point on a given curve  
- OnMesh : Keeping Pt on Mesh / Point, Mesh  
- OnPlane : Keep a point on a given plane / Point, Plane  
- Pressure : A force normal to each triangle / Mesh, Strength  
- PolygonArea : SetArea (Volume の 2d ver)  
- RigidBody : RigidBody / Part(Mesh), Points(optional??)  
- Smooth : Smooth Mesh / Mesh  
- SolidCollide : collision between a pair of solid, 前でCrossReference / MeshA, MeshB  
- SolidPointCollide : Keep a set of points outside or inside a given Mesh, Collision / pointList, Solid(brep or Mesh), Strength  
- SphereCollide : Collisions between large numbers of equal sized spheres / Point, Radius(Multi-Radius NG? Collider と違う)  


#### Main  
- Grab : ?  
- Solver : Goal をまとめて計算  / GoalObjects  
- Solver(bouncy) : Solver with momentum(弾力、弾み) / GoalObjects  
- StepSolover : アニメーション?  
- ZombieSolver : used in conjunction with "Garapagos"
- Show : Show  


#### ?  
- AlignFaces : align faces of a pair of rigid body  
- Beam : beam resisting bending and torsion  
- Bomb : causes an explosion after given number of iterations / Location(explosion), Points(Affected by explosion), Detonation(FrameCount)  
- CombineAndClean : Combine and Clean a list of meshes, removing unused and duplicate  
- Concentric : align axis of a pair of rigid body  
- Diagonalize : Replace each edge with a new face / Mesh  
- EdgeLength : Set edge length / Mesh  
- G2 : maintain curvature continuity between 2 nurbs curves / Points  
- Hinge : Hinge  
- HingePoint : get the 4 points for erch internal edge to use in a hinge force  
- ImageCircle : Circle packing with sizes from image colours / Mesh(with color), Crvs(area)  
- LoadVertex : Load に近い / Mesh, Strength(上or下)  
- Planarize  
- removeDuplicatePts : Removes Similar points from a list / P(List of points to clean)  
- Rod : Resistant rod, Angle に似てる  
- RigidPointSet : a set of points which maintain their relative positions  
- SoapFilm : area minimizing triangle, for generating zero mean curvature meshes, 領域が最小で、曲率が均一なメッシュ  
- SolidPlaneCollide : Collision between a plane and a solid, Floor に近い?  
- SplitAtCorners : break a polyline into multiple parts based "on angle" / Polyline, points(out)  
- Support : set support conditions for a beam end or rigid body  
- TangentialSmooth : smooth a mesh only in the local tangent plane, used in conjunction with "soapfilm"  
- Volume : set volume / Mesh(mesh), Volume(value)  
- Wind : Setting Wind / Mesh, WindVector  
- WrapWeft : separate the edges of a mesh into 2 list according to wrap and weft direction / Mesh, ListA(out), ListB(out)  







---  

---  


## Grasshopper Components  

#### Params  
- Garapagos : genetic algorism / GeneticInput, FitnessInput  

#### Curve  
- Curvature Graph : Draws Rhino Curvature Graphs(曲率)  
- Discontinuity : Find all dis-continuities along a curve  


#### Math  
- Average : Solve the arithmetic average for a set of items  
- Entwine : Flatten and combine a collection of data streams  
- Weave : Weave a set of input data using a custom pattern / P(pattern), data1, data2  

#### Surface  
- Surface Closest Point : Find the Closest point on surface / Point, Surface, uvP(out, PlaneNormal につなぐとよい)  


#### Mesh  
 - Mesh WeldVertices : merge identical vertices, 同じ頂点をマージ(weld 溶接)  


#### Vector  
- Closest Point : Find closest point in a point collection /P(Point), C(Cloud Point to search)  
- Closest Points : Find closest points in a point collection / P(Point), C(Cloud Point to search),T   
- Cull Duplicate : Cull point that are coincident within torerance / points(list of point)  
- PlaneNormal : Create a plane perpendicular to a vector  


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
