This tutorial is a two-in-one, it shows how to draw 2D Sprites for UI,
and how to draw dynamic font on the screen. The text in the font
can be changed at any time. This tutorial will use procedurally generated
geometry, so that means we don't need to build meshes for these
objects. The steps we will go through is similar to previous tutorials. New
pipeline, new shaders, new descriptor set, and this time, 
a new type of uniform buffer. This pipeline will not have a pVertexInputState
because the vertex buffer is procedurally generated in GLSL. We will need
an input assembly state, to give topology.This new pipeline will use 
TRIANGLE_STRIP instead of TRIANGLE_LIST, so that we can draw a 
quad with 4 vertices

Tutorial 17 was made on the last day of my coop, and it was mildly rushed, 
but there are no memory leaks, and the Vulkan validator returns no errors. 
It does everything it is supposed to do. There is room for improvement. 
This tutorial draws a 2D User-Interface over the 3D scene. 
With PNG sprites,  and dynamic fonts, which are both rendered 
procedurally (without vertex or index buffer). Also, the font uses Instanced 
Rendering, where each letter is a separate instance. The material in this 
tutorial can also be used in a 2D game engine.