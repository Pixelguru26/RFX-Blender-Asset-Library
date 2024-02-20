# RFX Blender Asset Library
 A fully open source modeling, geonodes, and shader library for Blender!
 Designed with an emphasis on science fiction and hard surface modeling, but contains a diverse range of essential tools. Designed for use with Blender 4.0 and the newly-added asset library feature.

 All assets are free to use, modify, and redistribute as you please. This toolkit is intended to provide a standard universal toolkit for all creators, regardless of background.

Highlights include:
- Circular array modifier (see "Simple Angular Array")
- Inset Faces geometry node implementation
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
		- Primitive
			- Advanced Circle
				> Constructs a mesh circle with additional options to exactly match a specified surface area, average radius, or other parameters.
			- Arrow Primitive
				> Constructs a simple arrow mesh pointing along a specified vector. Primarily a debug utility.
			- Bezier Arc
				> Constructs an approximate arc of a circle using bezier curves.
			- Bezier Circle
				> Constructs a standard approximate bezier circle.
			- Capsule
				> Constructs a simple capsule mesh.
			- Circle of Circles
				> Constructs a set of mesh circles with centers lying at regular intervals along the perimeter of a specified circle. By default, the smaller circles will be scaled to touch edges.
			- Curve Stadium
				> Constructs a geometric stadium shape ( see https://en.wikipedia.org/wiki/Stadium_(geometry) ) using Bezier curves.
			- Gear Primitive
				> Constructs a simple gear mesh with the specified number and interval of teeth.
			- Mesh Volumetric Grid
				> Constructs a cubic lattice of interconnected points with a specified resolution and size.
			- Roundcube
				> Constructs a sphere using subdivided cube topology.
	- Shading
	- Full easing nodes as defined by https://easings.net/
		> The geometry node versions are prefixed with a capital G.
- Meshes
	- Bolt Heads
		- Phillips
		- Slotted
		- Hex
	- Scaffolding unit
		> Full high resolution model heavily based on modern tower cranes.
	> Further catalogue to be written as mesh collection expands.
- Materials
	- Basic metals
		- Gold
		- Copper
		- Cobalt
	- Textured metals
		- Beaten copper
		- Weathered Aluminium
			> Visibly crystallized. Based on exposed infrastructural aluminium poles, such as flag poles, traffic lights, and sign posts.
		- Cast Iron
		- Cast Aluminium

Special thanks to @NinthDesertDude for assistance, direct contributions, and emotional support. ❤