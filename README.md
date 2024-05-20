# RFX Blender Asset Library
 A fully open source modeling, geonodes, and shader library for Blender!
 Designed with an emphasis on science fiction and hard surface modeling, but contains a diverse range of essential tools. Designed for use with Blender 4.0 and the newly-added asset library feature.

 All assets are free to use, modify, and redistribute as you please. This toolkit is intended to provide a standard universal toolkit for all creators, regardless of background. Suggestions are more than welcome!

 Asset contributions are also accepted with the only caveat that submitting them grants permission to all users of this library now and in the future to do as they please with them, in the spirit of open collaboration. Attribution will be provided in this readme.

Highlights include:
- Circular array modifier (see "Simple Angular Array")
- Inset Faces geometry node implementation
- Adjustable panels, bars, and greebles
- Curve deformation modifier
- Full set of easing nodes

### Contents
- Nodes
	- Geometry
		- Modifiers
			- Frame Resizing
				- Frame Extend
				- Advanced Frame Resize
				- Directional Frame Resize
			- Arrays
				- Simple Angular Array
					> Arranges n instances of an object around its center point. Argued by some to be the most useful item in this entire toolkit.
				- Fully Interpolated Array
					> An array modifier which interpolates completely between two positions and rotations.
				- Array
					> A simple array modifier implemented in geometry nodes.
				- Array Fill
					> An array modifier node which attempts to fill an exact cuboid with instances of the input mesh.
			- Deformations
				- Fit Bounding Box
					> Scales a mesh along the XYZ axes to fit a bounding box.
				- Cast to Sphere
					> scales the distance of each vertex of a mesh from the center to lie along a perfect sphere.
				- Curve Deform
					> Deforms a given mesh along one of the major axes to conform to a curve.
			- Curve Tools
				- Bezier Debug Visualization
					> A modifier which constructs a mesh to visualize all control points of a Bezier curve.
				- Join Bezier Curves
					> Joins Bezier curves end-to-end. Preserves control points, radius, and tilt. Does not necessarily preserve other attributes yet. Does not work well with other types of curves.
				- Join Poly Curves
					> Joins poly curves end-to-end with new edges. Preserves radius and tilt. Does not preserve other attributes yet. Converts all other curves to minimum-resolution polyline versions.
				- Set Bezier Point (+relative)
					> Combines full control of Bezier curve control nodes and associated left/right control points by index. The relative variant uses relative positions and is the recommended form for manual operation.
			- Effect
				- Cable
					> Converts a curve into a mesh with multiple wound strands. Ideal for simple rope and steel cable.
				- Chain Along Curve
					> Converts a curve into a set of chain link instances roughly aligned along its length.
				- Dotted Line
					> Converts a curve into a series of dashed mesh tubes with rounded ends. YMMV
			- Misc
				- Inset Faces
					> Attempts to replicate the equivalent mesh editing tool as a geometry node. Method used is vertex sliding along edge cross tangents.
				- Instance Along Curve
					> Instantiates objects onto a curve facing along the tangent.
				- Pinwheel
					> Extremely powerful modifier which transforms geometry to conform to a curve and arrays it around a circle.
					> Intended usage: construct a section of a wheel/other round object with intended result pattern, subdivide, and apply modifier.
					- Lateral index: axis transformed into a curve. Anything aligned along this axis will end up at the same radius.
					- Radial index: axis defining radius. Anything aligned along this axis will end up at the same angle.
					- Axis index: axis of rotation. Anything aligned on this axis will stay aligned.
				- Relathe
					> Reconstructs a rotationally-symmetrical object with a new angular resolution.
					> Cuts the object into a profile curve and rotates it at new intervals.
					> Currently may cause inconsistent normals. Looking into it.
				- Screw
					> Operates much like the stack modifier.
					> Currently only operates on Z axis.
				- Wedge Ring
					> I'll be honest, I forgot how this worked. Documentation to come later.
		- Utilities
			- Proximity Select
			- Sample Nearest Point
			- To Global Coords
				> Converts a coordinate vector to its global environment equivalent using transformation information about an object. WIP.
			- Advanced Bounding Box
				> Constructs a bounding box around a mesh and returns information about it. Includes dimensions and instance realization as well as vanilla features.
		- Math
			- Alternate
				> Alternates between true and false at regular intervals of the input factor.
			- Approach
				> Returns a value closer to the target than the input by a maximum of an exact delta. Snapes to the target when the delta exceeds distance to the target.
			- Calc Array Fill
				> Calculates information used to fill a cuboid volume with smaller cuboids.
			- Project to Plane
				> Projects a vector onto the plane of the specified normal vector.
			- Mix 3
			- Rectangle
			- Triple Switch
			- Triple Switch Vector
			- Vector Coordinate System Transform
			- Vector Select
				> Selects a single component of a vector given an input of 0-2.
			- Vector Swizzle
				> Shuffles vector components.
		- Primitives
			- Mesh Primitives
				- Advanced Circle
					> Constructs a mesh circle with additional options to exactly match a specified surface area, average radius, or other parameters.
				- Arrow Primitive
					> Constructs a simple arrow mesh pointing along a specified vector. Primarily a debug utility.
				- Capsule
					> Constructs a simple capsule mesh.
				- Circle of Circles
					> Constructs a set of mesh circles with centers lying at regular intervals along the perimeter of a specified circle. By default, the smaller circles will be scaled to touch edges.
				- Gear Primitive
					> Constructs a simple gear mesh with the specified number and interval of teeth.
				- Mesh Volumetric Grid
					> Constructs a cubic lattice of interconnected points with a specified resolution and size.
				- Roundcube
					> Constructs a sphere using subdivided cube topology.
				- Mesh Stadium
					> Constructs a clean stadium mesh which fits exactly within the provided dimensions.
					> If z is zero, produces 2d mesh only.
			- Curve Primitives
				- Bezier Arc
					> Constructs an approximate arc of a circle using bezier curves.
				- Bezier Circle
					> Constructs a standard approximate bezier circle.
				- Curve Stadium
					> Constructs a geometric stadium shape ( see https://en.wikipedia.org/wiki/Stadium_(geometry) ) using Bezier curves.
	- Shading
		- Coordinate Space Transforms
			- Cylindric Coords
			- Grid Coords
			- Spherical Coords
			- Polar Coords
		- Signed Distance Functions
			- Face SDF
			- Rhombic Dodecahedron SDF
		- Shader Effects
			- Hammered Normals
			- Parallax
			- SSS Glass BSDF
		- Math & Geometry
			- Project to Plane
			- Vector Sum
				> Signed scalar sum of vector components.
		- Misc
			- UV Hack - Closest Pole
	- Full easing nodes as defined by https://easings.net/
		> The geometry node versions are prefixed with a capital G.
- Meshes
	- Greebles
		- Realistic
			- Shelf Bracket
			- Mounting Plate
			- Rocketdyne Inspired RCS Block
		- Scifi & Technical
			- Articulated Block
			- Curved Blade
			- Cog Chuck
			- Coil
			- Cylindrical Mount
			- Radial Grate
			- Pipe Array
			- Handlebar (adjustable)
			- Industrial Cable Mount
			- Riveted Square
			- Joint Socket
			- Round Vent Panel
			- Slotted Wheel
			- Heavy Duty Wheel
			- Container Slide
			- Mountable Side Thruster
		- Bolt Heads
			- Phillips
			- Cross Notch
			- Slotted
			- Hex
			- Flanged Hex
			- Bevel Crowned Hex
			- Rivet
			- Micro Rivet (ultra low poly)
		- Ninth Desert Dude Contributions
			- Symbols (6 iconographic meshes)
			- Structural
				- Stackable Art Trellis
				- Simple Wall Support
				- Fan + Case
				- Twisted Pillar
				- Twisted + Tapered Pillar
				- Wall Lattice
				- Wall Vanes
	- Structures
		- Scaffolding unit
			> Full high poly model heavily based on modern tower cranes.
		- Platform Scaffold
			> Scaffolding unit commonly used for storage or contractor work.
	> Further documentation to be provided as time allows. Many more are included than written.
- Materials
	- Basic metals
		> None of these require UV maps.
		- Cobalt
		- Copper
		- Gold
	- Textured metals
		> None of these require UV maps.
		- Cast Aluminium
		- Weathered Aluminium
			> Visibly crystallized. Based on exposed infrastructural aluminium poles, such as flag poles, traffic lights, and sign posts.
		- Cast bronze
		- Beaten copper
		- Cast Iron
	- SF Collection
		> A collection of fantasy and semi-realistic materials designed for visual appeal rather than realism.
		> None of these require UV maps as of now.
		- Black Rubber
			> Smooth black rubber with a dull surface. Intended for use in hoses, pads, cables, and other such details.
		- Industrial Metal (Painted)
			> Basic heavy metal using color attribute to apply paint. Intended for previews or vertex-colored models.
		- Marble
			> Polished white marble with multiple layers of detail.
		- Mesh
			> Perforated steel mesh using 3d packing to avoid the need for UV maps. Intended for use on low-poly meshes.
		- Red Granite
			> Polished red granite with multiple layers of detail.
		- Ruin Alloy
			> Grungy brown metal.
		- Rusty Patch Steel
			> Basic steel with irregular patches of rust.
		- Tempered Glass
			> Custom smooth glass shader with depth-based blue tinting.
			> Optimized for Cycles, does little in Eevee.
		- Concrete (WIPCrete)
			> WIP procedural worn concrete.
		- Concrete (Painted)
			> WIP cheap concrete coated in paint, uses vertex colors.
		- Simple Bars
			> Simple crossed metal bars with normal maps and open spaces. Intended for use on low-poly meshes.

Special thanks to @NinthDesertDude for assistance, direct contributions, and emotional support. ❤