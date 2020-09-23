<div align="center">

## An Introduction To DirectX 8 \- And More\!\!\!


</div>

### Description

<h4><font color="#FF0000">Learn every aspect of DirectX8 now!</font></h4>

<p><font color="#000000">This <b>HUGE </b>tutorial covers DirectX 8,

DirectSound8, DirectInput8, Direct3D8. It includes everything - from knowing

nothing to having a good grasp of DirectX 8 with Visual Basic. It even goes

beyond that and explains the logic needed to create 3D geometry and animation.

There is a fully documented sample program too! And a glossary of terms - not

just DirectX terms - but general programming and 3D mathematics too! The best

DirectX 8 tutorial you are ever gonna get for free! Even people who already know

DirectX should read this, as it goes onto more complex subjects. Especially

people who have learnt DirectX 7 or earlier.</font></p>

<p><font color="#000000">Please remember to give me lots of feedback and votes

so I know how to make future tutorials!</font></p>
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Simon Price](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/simon-price.md)
**Level**          |Beginner
**User Rating**    |4.9 (247 globes from 50 users)
**Compatibility**  |VB 6\.0
**Category**       |[DirectX](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/directx__1-44.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/simon-price-an-introduction-to-directx-8-and-more__1-14218/archive/master.zip)





### Source Code

<h1 align="center">An Introduction To DirectX8</h1>
<h3 align="center">By <a href="mailto:Si@VBgames.co.uk">Simon Price</a></h3>
<p align="center">Visit <a href="http://www.VBgames.co.uk">www.VBgames.co.uk</a>
for more!</p>
<h4>What you will learn</h4>
<ul>
 <li>How to use the DirectX libraries from Visual Basic</li>
 <li>How to get input from the most commonly used devices - keyboard and mouse
  - using DirectInput</li>
 <li>How to load and play a wave file using DirectSound</li>
 <li>How to create a rendering device with Direct3D</li>
 <li>How to use the D3DX helper functions</li>
 <li>How to use vertex and index buffers to create simple geometry</li>
 <li>How to use view and projection matrices to set up a camera</li>
 <li>How to use world matrices to make animation and reuse the same geometry</li>
 <li>How to load textures from a bitmap file</li>
 <li>How to unload all of this safely</li>
</ul>
<h4>How you will learn it</h4>
<ul>
 <li>Overview of DirectX8</li>
 <li>Explanation of DirectX terms</li>
 <li>Explanation of sample program</li>
 <li>Full working demo program to <a href="http://www.VBgames.co.uk/tutorials/dx8intro.zip">download</a>
  with source code and comments</li>
 <li>Evaluation of what has been learnt</li>
 <li>Exercises to extend your knowledge</li>
 <li>Thoughts for future tutorials</li>
</ul>
<h4>Boring Intro</h4>
<p>Back by popular demand is my DirectX tutorial series! Although I'm sort of starting
again for DirectX 8. So for complete newbies, this tutorial is great, and for
those who already know some DX7 or DX8, the tutorial includes some more complex
stuff than previous tutorials. In DirectX 8, the API has become simpler in
the initialization of objects and it also has many more maths functions to help
you. But it's still alot of work to do by yourself, so that's why you should
help spread the word by making free source demos and tutorials. At this point I acknowledge
Richard Hayden for his free source Direct3D8 world, it is a great example of
what I am talking about and helped me begin to learn the new API. Enough of the
chit chat...</p>
<h4>Before you begin</h4>
<p>If you don't already have DirectX 8 and the DirectX 8 Type Libraries for
Visual Basic then you've got some downloading to do! Sorry, but it is worth it.
You don't need all the SDK documentation, although I recommend getting it, and
you don't need the C++ SDK if you are a VB'er only, so your download might not
be as big as mine was. I managed to download 135 MB though my cheap 56 K phone
line though, and that was the full download including everything. So it is
possible, but you will need to get a program such as <a href="http://www.getright.com">GetRight</a>
to help you download such a big file. All developer information and downloads
can be found at <a href="http://www.microsoft.com/directx">www.microsoft.com/directx</a>
. Once DirectX 8 is installed, and you have the DX VB Type Libs, read on.</p>
<h4>Adding a reference to your project</h4>
<p>Every time you start a new project that will use DirectX, you will need to do
the following:</p>
<ul>
 <li>Click the Project menu</li>
 <li>Choose the References... submenu and the References dialog will pop up</li>
 <li>Scroll down the list of references until you find the &quot;DirectX 8 Type
  Library for Visual Basic&quot; and check the box next to it</li>
 <li>Click OK</li>
</ul>
<p>Now VB will know every class, type and enumeration that DirectX 8 contains,
so you're ready to begin coding!</p>
<h4>DirectX and 3D terminology</h4>
<p>This is the part which gets most people. I wish I had someone to explain all
the jargon to me when I was learning. After the language barrier, things get a
bit easier. Here's some terms you need to know. If you already know a bit about
DirectX, you should probably skip this whole section and only come back to it
when you see a word you don't understand. It is not in alphabetical order,
rather it is in logical order so that you can read the whole thing if you're new
and you want to. As you can see, there is alot of it, and this is only the basics.</p>
<ul>
 <li><i>DirectX, DirectAudio (DirectSound, DirectMusic), DirectGraphics
  (Direct3D, DirectDraw), DirectPlay, DirectSetup </i>- These are all part of
  the DirectX API. They are the main objects which deal with different jobs
  e.g DirectAudio takes care of all audio input and output, and it contains
  DirectSound and DirectMusic</li>
 <li><i>API </i>- What does that stand for again? I think it was Advanced
  Programming Interface (correct me please if I'm wrong). At least I know what
  it means. It's the bunch of objects that give you a higher level view of a
  task, so you don't need to think about writing low level code anymore
  because people have already made functions to do that for you.</li>
 <li><i>Variable </i>- If you don't know what a variable is, go away and learn
  something simpler.</li>
 <li><i>Type </i>- I hope you know this too. It's several variables group
  together, in C++ it's a structure.</li>
 <li><i>Class </i>- This is code that describes an object (see below).</li>
 <li><i>Object </i>- An object can contain variables like a type, but it also
  can have functions that can be called from code elsewhere. An object is
  created from a class.</li>
 <li><i>Instance </i>- When an object is created from a class, it is said to be
  an instance of the object. Note there can be many instances of an object
  created from the same class.</li>
 <li><i>Library - </i>A whole group of objects are often grouped together into
  one file, usually a DLL (Dynamic Link Library). DirectX is made of DLL's.</li>
 <li><i>Pointer </i>- This is a variable that stores a memory address. In VB,
  your don't use pointers directly, but if you use a object without creating a
  new instance of the object, you are basically using a pointer to another
  object.</li>
 <li><i>Buffer </i>- A word given to a chunk of memory which has been assigned
  a job, usually to temporarily store data which is moved around alot. There
  are several types of buffer in DirectX.</li>
 <li><i>Backbuffer, Frontbuffer, Surface, Texture - </i>These are used to store
  graphics. The only visible graphics buffer is the front buffer. In DirectX
  8, you never need to worry about this, just know what it is (erm, like, it's
  what you see on the screen). A back buffer is where graphics go just before
  the front buffer. You draw on the back buffer, and when your super duper
  graphics are finished, you ask DirectX to move it to the front buffer. A
  surface is just like a back buffer, it stores pictures, but it is more
  general since it has nothing to do with a front buffer. A texture is a
  surface used for texture mapping polygons (see later), and is usually of dimensions
  that are square, a power of 2, typically 256 x 256.</li>
 <li><i>Copy, VSync, Blt, Flip, Discard </i>- These are methods of copying from
  one surface to another. Copying involves copying every single bit from on
  surface to another. Flipping involves moving a pointer to s surface so that
  the front buffer and back buffer surfaces switch roles (their pointers are
  swapped) making for a very quick appearance of a new image. VSync means synchronizing
  the copying or flipping of surfaces with the vertical refresh of the monitor
  so that you can't see the graphics flicker. If you discard your surface when
  you flip, it is a faster, but the contents of the back buffer are not
  guaranteed to be still the same as before the flip.</li>
 <li><i>Z buffer </i>- A piece of memory that store the z positions of objects
  drawn onto a surface.</li>
 <li><i>Sound buffers (primary and secondary) </i>- A sound buffer stores a
  sound. A primary sound buffer can be heard out of the speakers, with DirectX
  you can ignore it because it is managed for you. A secondary sound buffer is
  where sounds can be stored before being mixed and sent to the primary
  buffer.</li>
 <li><i>Mixing </i>- The process of creating just one sound from several source
  sounds.</li>
 <li><i>Static and streaming </i>- A static buffer stores just a whole sound
  and just sits there. A streaming buffer stores only part of the sound and
  constantly is moving in the next part of the sound and and moving out the
  already played sound. A static buffer is more CPU efficient and a streaming
  buffer is more memory efficient.</li>
 <li><i>Input device </i>- This is commonly a mouse or a keyboard, but can also
  be a joy pad or a steering wheel etc.</li>
 <li><i>Device state </i>- The state of the input device depends on what
  buttons/rollers/wheels are being pressed/moved etc. For example, the state
  of the keyboard is that the &quot;X&quot; key is down.</li>
 <li><i>Rendering device </i>- This is something that draws graphics, it can be
  a hardware graphics card or a software emulation device.</li>
 <li><i>Hardware and software emulation </i>- Hardware is a physical unit on
  your computer and is usually very fast at doing it's job. Software emulation
  can do the same job as hardware, but at a slower rate and using up memory.</li>
 <li><i>System and video memory </i>- System memory is the main memory where everything
  else is stored - programs, Windows, anything and everything scattered
  everywhere so it can be slow. Video memory is separately used for hardware
  to store pictures and is usually alot faster. It can be a slow operation to
  copy between these two types of memory.</li>
 <li><i>Polygon, Primitive </i>- Polygons are a general term for shapes that
  can be made with a number of straight edged sides and are used in 3D store
  create shapes. In Direct3D, a primitive is usually a point, a line or a
  triangle.</li>
 <li><i>Material </i>- A polygon appears to be made of a material, in DirectX,
  a material has several colors to describe it's appearance.</li>
 <li><i>Texture mapping </i>- When a polygon has a picture put onto it it is
  said that the polygon has been texture mapped.</li>
 <li><i>Texture management</i> - Textures must be ordered and and moved around
  so that the right textures are available when they are need. DirectX by
  default can do this for you.</li>
 <li><i>Vector </i>- A 3 dimensional value, having x, y and z components.</li>
 <li><i>Vertex </i>- A primitive is made up of vertices (plural of vertex)
  where edges end or meet. They can be just the same as vectors, or they can
  have additional components such as color, direction (or normal), or texture
  coordinates.</li>
 <li><i>Plane </i>- A flat shape that goes on forever and splits space into 2.
  For example, the ground is a horizontal plane.</li>
 <li><i>Normal </i>- A normal to a plane or vertex or primitive is a vector
  that describes where it is facing. Has a similar meaning as perpendicular or
  orthogonal. </li>
 <li><i>Transformation </i>- A formula that changes a vector to another
  position.</li>
 <li><i>Matrix </i>- Matrices (plural of matrix) describes any transformation
  by storing 16 numbers.</li>
 <li><i>Translation, rotation, scaling </i>- These are types of
  transformations. A translation is a movement in the x, y or z direction (or
  2 or all 3 directions), a rotation spins the vector around an origin,
  scaling resizes the vector around a origin.</li>
 <li><i>Origin</i> - A point or vector that is the center of something.</li>
 <li><i>World, View and Projection </i>- The world transformation affects every
  vector in the world, moving it moves everything. The view transformation
  makes the camera or eye on the scene appear to be in the right place, and
  the projection transformation describes how the 3D scene is conveyed onto
  the 2D picture produced from it.</li>
 <li><i>Culling</i> - When a polygon is not facing the camera, the process of
  culling ensures it is not drawn.</li>
 <li><i>Z buffering and Z sorting </i>- This process makes sure that when a
  object is obscured by another, it cannot be seen.</li>
 <li><i>More...</i> I've missed out loads so if you still don't understand a
  word then just ask.</li>
</ul>
<h4>The sample program</h4>
<p>You can download the sample program from <a href="http://www.VBgames.co.uk/tutorials/dx8intro.zip">here</a>.
You will need a program like <a href="http://www.winzip.com">Winzip</a> to
decompress it. It is written in Visual Basic 6, if you have another version of
VB then there is information on <a href="http://www.planet-source-code.com/vb">www.planet-source-code.com/vb</a>
as to how to try to open the version 6 files.</p>
<p>The sample program uses hardware accelerated rasterization. If your computer does not have this, the request
will fail, so use D3DDEVTYPE_REF instead of D3DDEVTYPE_HAL if this happens. A real
program would be able to detect an error and automatically switch device. It also requests software vertex processing, which means the CPU has to
transform and light geometry, but if you have a good graphics card, you might be
able to use hardware vertex processing.&nbsp;</p>
<p>The sample program assumes your computer can render in 16 bit (R5G6B5) color
format, in 640 x 480 resolution. If this is not the case, it may fail but you
can change those values in the source code.</p>
<p>The sample program renders the same texture mapped 3D cube in different
positions. It uses the same cube but it makes it appear that there are 3, each
of different sizes, and they are all spinning and rotating around everywhere.
The camera can be zoomed in and out using the mouse and the program can be
exited using the escape key. The program plays a sound every time the animation
loop restarts. It attempts to show all the basic features of DirectX 8 simply.
It is not optimized so as to keep it as simple to understand as possible.</p>
<p>The main point to note is the that the animation is achieved by moving the
world transformation. Every single line is commented, an there are lengthy
explanations of each main function. Here is the full source code and comment to
view, but you can also <a href="http://www.VBgames.co.uk/tutorials/dx8intro.zip">download</a>
it.</p>
<p>---***---SOURCE CODE STARTS HERE---***---</p>
<p><font color="#008000">'-----------------------------------------------------------------<br>
'<br>
'  DX8 INTRODUCTION - DIRECTGRAPHICS,DIRECTSOUND, DIRECTINPUT<br>
'<br>
'             BY SIMON PRICE<br>
'<br>
'-----------------------------------------------------------------<br>
<br>
' For this tutorial program you will need the DirectX8 for Visual<br>
' Basic Type Library, from www.microsoft.com/directx<br>
<br>
' You should also have the tutorial in HTML format, if you don't<br>
' you can download it from my website www.VBgames.co.uk<br>
<br>
' Any questions go to ihaveaquestionforsimonaboutdx8@VBgames.co.uk,<br>
' or you could use a shorter address :) (si@VBgames.co.uk will do)<br>
' Any bug reports go to the same address too please, as do comments<br>
' feedback, suggestions, erm whatever you feel like<br>
<br>
' Every time you start a project which will use DirectX8, you need<br>
' to click on the menu Project -> References and a dialog box will<br>
' pop up. Check the box which says "DirectX8 for Visual Basic Type<br>
' Library" and click OK. Now VB will know all the types, classes<br>
' enumerations and functions of DirectX8.<br>
</font><br>
Option Explicit<br>
<br>
<font color="#008000">' GLOBAL VARIABLE DECLARATIONS<br>
<br>
' No matter what you do with DirectX8, you will need to start with<br>
' the DirectX8 object. You will need to create a new instance of<br>
' the object, using the New keyword, rather than just getting a<br>
' pointer to it, since there's nowhere to get a pointer from yet (duh!).<br>
</font><br>
Dim DX As New DirectX8<br>
<br>
<font color="#008000">' The DirectInput8 object is used to get data from input devices<br>
' such as the mouse and keyboard. This is what we will use it for<br>
' in this tutorial, since they are the most common input devices.<br>
' Notice how we don't create a new instance of the object, rather<br>
' DirectX does that for us and we just get a pointer to it.<br>
</font><br>
Dim DI As DirectInput8<br>
<br>
<font color="#008000">' Now we need 2 devices - keyboard and mouse...<br>
</font><br>
Dim Keyboard As DirectInputDevice8<br>
Dim Mouse As DirectInputDevice8<br>
<br>
<font color="#008000">' ...and a structure (type) to hold the data from each device. DI<br>
' provides us a custom keyboard and mouse type, since they are<br>
' commonly used<br>
</font><br>
Dim KeyboardState As DIKEYBOARDSTATE<br>
Dim MouseState As DIMOUSESTATE<br>
<br>
<font color="#008000">' Next, we have DirectSound8, this can be used for many things, but<br>
' for now we just play a sound from a .wav file<br>
</font><br>
Dim DS As DirectSound8<br>
<br>
<font color="#008000">' A sound buffer is a piece of memory in which the sound is stored.<br>
' We use a secondary buffer, because a primary buffer can actually<br>
' be heard though the speakers, and the sound needs to be mixed<br>
' before we allow the user to hear that. In this tutorial, we let<br>
' DirectSound worry about mixing and copying to the primary buffer<br>
' to play the sound for us<br>
</font><br>
Dim Sound As DirectSoundSecondaryBuffer8<br>
<br>
<font color="#008000">' The DSBUFFER type holds a description of a sound buffer. We won't<br>
' use any of the more advanced flags in this tutorial<br>
</font><br>
Dim SoundDesc As DSBUFFERDESC<br>
<br>
<font color="#008000">' The Direct3D8 object is responsible for all graphics, yes, even 2D<br>
</font><br>
Dim D3D As Direct3D8<br>
<br>
<font color="#008000">' The D3DX8 object contains lots of helper functions, mostly math<br>
' to make Direct3D alot easier to use. Notice we create a new<br>
' instance of the object using the New keyword.<br>
</font><br>
Dim D3DX As New D3DX8<br>
<br>
<font color="#008000">' The Direct3DDevice8 represents our rendering device, which could<br>
' be a hardware or a software device. The great thing is we still<br>
' use the same object no matter what it is<br>
</font><br>
Dim D3Ddevice As Direct3DDevice8<br>
<br>
<font color="#008000">' The D3DPRESENT_PARAMETERS type holds a description of the way<br>
' in which DirectX will display it's rendering<br>
</font><br>
Dim D3Dpp As D3DPRESENT_PARAMETERS<br>
<br>
<font color="#008000">' The D3DMATERIAL8 type stores information on the material our<br>
' polygons are rendered with, such as color<br>
</font><br>
Dim Material As D3DMATERIAL8<br>
<br>
<font color="#008000">' The Direct3DTexture8 object represents a piece of memory used to<br>
' store a texture to be mapped onto our polygons<br>
</font><br>
Dim Texture As Direct3DTexture8<br>
<br>
<font color="#008000">' The Direct3DVertexBuffer8 object stores an array of vertices from which<br>
' our polygons are made<br>
</font><br>
Dim VertexBuffer As Direct3DVertexBuffer8<br>
<br>
<font color="#008000">' The D3DVERTEX type stores vertices temporarily before we copy<br>
' them into the vertex buffer<br>
</font><br>
Dim Vertex(1 To 24) As D3DVERTEX<br>
<br>
<font color="#008000">' The Direct3DIndexBuffer8 object stores the order in which our<br>
' vertices are rendered<br>
</font><br>
Dim IndexBuffer As Direct3DIndexBuffer8<br>
<br>
<font color="#008000">' These integers are used to temporarily store indices before they<br>
' are copied into the index buffer<br>
</font><br>
Dim Index(1 To 36) As Integer<br>
<br>
<font color="#008000">' This stores the rotation of the cubes<br>
</font><br>
Dim Rotation As Single<br>
<br>
<br>
<br>
<br>
<br>
<br>
<font color="#008000">' FORM_LOAD<br>
<br>
' The whole program is started and controlled from here<br>
</font><br>
Private Sub Form_Load()<br>
&nbsp;&nbsp;&nbsp; On Error Resume Next<br>
<font color="#008000">&nbsp;&nbsp;&nbsp;</font> <font color="#008000">' initialize directx<br>
&nbsp;&nbsp;&nbsp; </font>If Init = False Then<br>
<font color="#008000">&nbsp;&nbsp;&nbsp;</font>&nbsp;&nbsp;&nbsp;&nbsp; <font color="#008000">' display error message<br>
</font>&nbsp;&nbsp;&nbsp;<font color="#008000">&nbsp;&nbsp;&nbsp;&nbsp; </font>MsgBox "Error! Could not initialize DirectX!"<br>
&nbsp;&nbsp;&nbsp; Else<br>
<font color="#008000">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ' show form<br>
</font>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Show<br>
<font color="#008000">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ' do main program loop<br>
</font>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; MainLoop<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; End If<br>
<font color="#008000">&nbsp;&nbsp;&nbsp; ' unload form and clean up directx<br>
</font>&nbsp;&nbsp;&nbsp; Unload Me<br>
End Sub<br>
<br>
<br>
<font color="#008000">' FORM_UNLOAD<br>
<br>
' Before the program ends, call the cleanup function<br>
</font><br>
Private Sub Form_Unload(Cancel As Integer)<br>
  CleanUp<br>
End Sub<br>
<br>
<br>
<br>
<br>
<br>
<font color="#008000">' INITIALIZATION<br>
<br>
' In this function we initialize all the global DirectX objects. We<br>
' basically get the DirectInput, DirectSound, and DirectGraphics<br>
' engines started up, and retrieve pointers so we can manipulate them<br>
</font><br>
Function Init() As Boolean<br>
<br>
&nbsp;&nbsp;&nbsp; 'On Error GoTo InitFailed<br>
<br>
<font color="#008000">&nbsp;&nbsp;&nbsp;</font> <font color="#008000">' DIRECTINPUT<br>
</font><br>
<font color="#008000">&nbsp;&nbsp;&nbsp;</font> <font color="#008000">' Get a pointer to DirectInput<br>
&nbsp;&nbsp;&nbsp; </font>Set DI = DX.DirectInputCreate()<br>
<font color="#008000">&nbsp;&nbsp;&nbsp;</font> <font color="#008000">' Check to see if the pointer is valid<br>
&nbsp;&nbsp;&nbsp; </font>If DI Is Nothing Then GoTo InitFailed<br>
<br>
<font color="#008000">&nbsp;&nbsp;&nbsp;</font> <font color="#008000">' Get a pointer to keyboard and mouse device objects<br>
&nbsp;&nbsp;&nbsp; </font>Set Keyboard = DI.CreateDevice("GUID_SysKeyboard")<br>
&nbsp;&nbsp;&nbsp; Set Mouse = DI.CreateDevice("guid_SysMouse")<br>
<font color="#008000">&nbsp;&nbsp;&nbsp; ' Check to see if pointers are valid<br>
</font>&nbsp;&nbsp;&nbsp; If Keyboard Is Nothing Then GoTo InitFailed<br>
&nbsp;&nbsp;&nbsp; If Mouse Is Nothing Then GoTo InitFailed<br>
<br>
<font color="#008000">&nbsp;&nbsp;&nbsp; ' Set the data formats to the commmonly used keyboard and mouse<br>
</font>&nbsp;&nbsp;&nbsp; Keyboard.SetCommonDataFormat DIFORMAT_KEYBOARD<br>
&nbsp;&nbsp;&nbsp; Mouse.SetCommonDataFormat DIFORMAT_MOUSE<br>
<br>
<font color="#008000">&nbsp;&nbsp;&nbsp; ' Set cooperative level, this tells DI how much control we need<br>
</font>&nbsp;&nbsp;&nbsp; Keyboard.SetCooperativeLevel hWnd, DISCL_NONEXCLUSIVE Or DISCL_BACKGROUND<br>
&nbsp;&nbsp;&nbsp; Mouse.SetCooperativeLevel hWnd, DISCL_NONEXCLUSIVE Or DISCL_BACKGROUND<br>
<br>
<font color="#008000">&nbsp;&nbsp;&nbsp; ' Now we are ready to aquire (erm, get) our input devices<br>
</font>&nbsp;&nbsp;&nbsp; Keyboard.Acquire<br>
&nbsp;&nbsp;&nbsp; Mouse.Acquire<br>
<br>
<font color="#008000">&nbsp;&nbsp;&nbsp; ' DIRECTSOUND<br>
<br>
&nbsp;&nbsp;&nbsp; ' Get a pointer to DirectSound<br>
</font>&nbsp;&nbsp;&nbsp; Set DS = DX.DirectSoundCreate("")<br>
<font color="#008000">&nbsp;&nbsp;&nbsp; ' Check the pointer is valid<br>
</font>&nbsp;&nbsp;&nbsp; If DS Is Nothing Then GoTo InitFailed<br>
<br>
<font color="#008000">&nbsp;&nbsp;&nbsp; ' Set cooperative level, we only need normal functionality<br>
</font>&nbsp;&nbsp;&nbsp; DS.SetCooperativeLevel hWnd, DSSCL_NORMAL<br>
<br>
<font color="#008000">&nbsp;&nbsp;&nbsp; ' Create a sound buffer from a .wav file. We provide a filename<br>
&nbsp;&nbsp;&nbsp; ' and a DSBUFFER type, which stores any special information<br>
&nbsp;&nbsp;&nbsp; ' about the buffer we might need to know (not used here)<br>
</font>&nbsp;&nbsp;&nbsp; Set Sound = DS.CreateSoundBufferFromFile(App.Path &amp; "\sound.wav", SoundDesc)<br>
<font color="#008000">&nbsp;&nbsp;&nbsp; ' Check the pointer is valid<br>
</font>&nbsp;&nbsp;&nbsp; If Sound Is Nothing Then GoTo InitFailed<br>
<br>
<font color="#008000">&nbsp;&nbsp;&nbsp; ' DIRECT3D<br>
<br>
&nbsp;&nbsp;&nbsp; ' Get a pointer to Direct3D<br>
</font>&nbsp;&nbsp;&nbsp; Set D3D = DX.Direct3DCreate()<br>
<font color="#008000">&nbsp;&nbsp;&nbsp; ' Check the pointer is valid<br>
</font>&nbsp;&nbsp;&nbsp; If D3D Is Nothing Then GoTo InitFailed<br>
<br>
<font color="#008000">&nbsp;&nbsp;&nbsp; ' Fill the D3DPRESENT_PARAMETERS type, describing how DirectX should<br>
&nbsp;&nbsp;&nbsp; ' display it's renders<br>
</font><br>
&nbsp;&nbsp;&nbsp; With D3Dpp<br>
<font color="#008000">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ' set the most common fullscreen display mode<br>
</font>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; .Windowed = False <font color="#008000"> ' the app is not in a window</font><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; .BackBufferWidth = 640 <font color="#008000"> '
the size of the screen</font><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; .BackBufferHeight = 480<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; .BackBufferFormat = D3DFMT_R5G6B5 <font color="#008000"> ' the color depth format (16 bit)</font><br>
<font color="#008000">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ' the swap effect determines how the graphics get from<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ' the backbuffer to the screen - note : D3DSWAPEFFECT_DISCARD<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ' means that every time the render is presented, the backbuffer<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ' image is destroyed, so everything must be rendered again<br>
</font>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; .SwapEffect = D3DSWAPEFFECT_DISCARD<br>
<font color="#008000">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ' request a 16 bit z-buffer - this depth sorts the scene<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ' so we can't see polygons that are behind other polygons<br>
</font>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; .EnableAutoDepthStencil = 1<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; .AutoDepthStencilFormat = D3DFMT_D16<br>
<font color="#008000">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ' 1 backbuffer<br>
</font>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; .BackBufferCount = 1<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; End With<br>
<br>
<font color="#008000">&nbsp;&nbsp;&nbsp; ' Create the rendering device. Here we request a hardware rasterization.<br>
&nbsp;&nbsp;&nbsp; ' If your computer does not have this, the request may fail, so use<br>
&nbsp;&nbsp;&nbsp; ' D3DDEVTYPE_REF instead of D3DDEVTYPE_HAL if this happens. A real<br>
&nbsp;&nbsp;&nbsp; ' program would be able to detect an error and automatically switch device.<br>
&nbsp;&nbsp;&nbsp; ' We also request software vertex processing, which means the CPU has to<br>
&nbsp;&nbsp;&nbsp; ' transform and light our geometry<br>
</font>&nbsp;&nbsp;&nbsp; Set D3Ddevice = D3D.CreateDevice(D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL,
hWnd,&nbsp; D3DCREATE_SOFTWARE_VERTEXPROCESSING, D3Dpp)<br>
<font color="#008000">&nbsp;&nbsp;&nbsp; ' check the pointer is valid<br>
</font>&nbsp;&nbsp;&nbsp; If D3Ddevice Is Nothing Then GoTo InitFailed<br>
<br>
<font color="#008000">&nbsp;&nbsp;&nbsp; ' Set rendering options<br>
</font>&nbsp;&nbsp;&nbsp; D3Ddevice.SetRenderState D3DRS_CULLMODE, D3DCULL_NONE<br>
&nbsp;&nbsp;&nbsp; D3Ddevice.SetRenderState D3DRS_ZENABLE, D3DZB_TRUE ' enable z buffering<br>
&nbsp;&nbsp;&nbsp; D3Ddevice.SetRenderState D3DRS_FILLMODE, D3DFILL_SOLID ' render solid polygons<br>
&nbsp;&nbsp;&nbsp; D3Ddevice.SetRenderState D3DRS_LIGHTING, True ' enable lighting<br>
&nbsp;&nbsp;&nbsp; D3Ddevice.SetRenderState D3DRS_AMBIENT, vbWhite ' use ambient white light<br>
&nbsp;&nbsp;&nbsp;&nbsp;<br>
<font color="#008000">&nbsp;&nbsp;&nbsp; ' Set the material properties<br>
</font>&nbsp;&nbsp;&nbsp; With Material.Ambient<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; .a = 1: .r = 1: .g = 1: .b = 1<br>
&nbsp;&nbsp;&nbsp; End With<br>
<br>
<font color="#008000">&nbsp;&nbsp;&nbsp; ' Create a texture surface from a file<br>
</font>&nbsp;&nbsp;&nbsp; Set Texture = D3DX.CreateTextureFromFile(D3Ddevice, App.Path &amp; "\texture.bmp")<br>
<font color="#008000">&nbsp;&nbsp;&nbsp; ' Check the pointer is valid<br>
</font>&nbsp;&nbsp;&nbsp; If Texture Is Nothing Then GoTo InitFailed<br>
<br>
<font color="#008000">&nbsp;&nbsp;&nbsp; ' Set the material and texture as the current ones to render from<br>
</font>&nbsp;&nbsp;&nbsp; D3Ddevice.SetMaterial Material<br>
&nbsp;&nbsp;&nbsp; D3Ddevice.SetTexture 0, Texture<br>
<br>
<font color="#008000">&nbsp;&nbsp;&nbsp; ' Create a vertex buffer, using default usage and specifying enough memory for 24 vertices of format&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;</font>
D3DFVF_VERTEX<br>
&nbsp;&nbsp;&nbsp; Set VertexBuffer = D3Ddevice.CreateVertexBuffer(24 * Len(Vertex(1)), 0, D3DFVF_VERTEX, D3DPOOL_DEFAULT)<br>
<font color="#008000">&nbsp;&nbsp;&nbsp; ' Check pointer is valid<br>
</font>&nbsp;&nbsp;&nbsp; If VertexBuffer Is Nothing Then GoTo InitFailed<br>
<br>
<font color="#008000">&nbsp;&nbsp;&nbsp; ' Create an index buffer, using default uage and specifying enough memory for 36 16 bit integers<br>
</font>&nbsp;&nbsp;&nbsp; Set IndexBuffer = D3Ddevice.CreateIndexBuffer(36 * Len(Index(1)), 0, D3DFMT_INDEX16, D3DPOOL_DEFAULT)<br>
<font color="#008000">&nbsp;&nbsp;&nbsp; ' Check pointer is valid<br>
</font>&nbsp;&nbsp;&nbsp; If IndexBuffer Is Nothing Then GoTo InitFailed<br>
<br>
<font color="#008000">&nbsp;&nbsp;&nbsp; ' Now we make a cube shape out of our vetices<br>
</font>&nbsp;&nbsp;&nbsp; Vertex(1) = MakeVertex(-1, 1, -1, 0, 0, -1, 0, 0)<br>
&nbsp;&nbsp;&nbsp; Vertex(2) = MakeVertex(1, 1, -1, 0, 0, -1, 1, 0)<br>
&nbsp;&nbsp;&nbsp; Vertex(3) = MakeVertex(-1, -1, -1, 0, 0, -1, 0, 1)<br>
&nbsp;&nbsp;&nbsp; Vertex(4) = MakeVertex(1, -1, -1, 0, 0, -1, 1, 1)<br>
&nbsp;&nbsp;&nbsp; Vertex(5) = MakeVertex(1, 1, -1, 0, 0, 1, 0, 0)<br>
&nbsp;&nbsp;&nbsp; Vertex(6) = MakeVertex(-1, 1, -1, 0, 0, 1, 1, 0)<br>
&nbsp;&nbsp;&nbsp; Vertex(7) = MakeVertex(1, -1, -1, 0, 0, 1, 0, 1)<br>
&nbsp;&nbsp;&nbsp; Vertex(8) = MakeVertex(-1, -1, -1, 0, 0, 1, 1, 1)<br>
<br>
&nbsp;&nbsp;&nbsp; Vertex(9) = MakeVertex(-1, 1, 1, -1, 0, 0, 0, 0)<br>
&nbsp;&nbsp;&nbsp; Vertex(10) = MakeVertex(-1, 1, -1, -1, 0, 0, 1, 0)<br>
&nbsp;&nbsp;&nbsp; Vertex(11) = MakeVertex(-1, -1, 1, -1, 0, 0, 0, 1)<br>
&nbsp;&nbsp;&nbsp; Vertex(12) = MakeVertex(-1, -1, -1, -1, 0, 0, 1, 1)<br>
&nbsp;&nbsp;&nbsp; Vertex(13) = MakeVertex(1, 1, -1, 1, 0, 0, 0, 0)<br>
&nbsp;&nbsp;&nbsp; Vertex(14) = MakeVertex(1, 1, 1, 1, 0, 0, 1, 0)<br>
&nbsp;&nbsp;&nbsp; Vertex(15) = MakeVertex(1, -1, -1, 1, 0, 0, 0, 1)<br>
&nbsp;&nbsp;&nbsp; Vertex(16) = MakeVertex(1, -1, 1, 1, 0, 0, 1, 1)<br>
<br>
&nbsp;&nbsp;&nbsp; Vertex(17) = MakeVertex(-1, 1, -1, 0, 1, 0, 0, 0)<br>
&nbsp;&nbsp;&nbsp; Vertex(18) = MakeVertex(1, 1, -1, 0, 1, 0, 1, 0)<br>
&nbsp;&nbsp;&nbsp; Vertex(19) = MakeVertex(-1, 1, 1, 0, 1, 0, 0, 1)<br>
&nbsp;&nbsp;&nbsp; Vertex(20) = MakeVertex(1, 1, 1, 0, 1, 0, 1, 1)<br>
&nbsp;&nbsp;&nbsp; Vertex(21) = MakeVertex(-1, -1, -1, 0, -1, 0, 0, 0)<br>
&nbsp;&nbsp;&nbsp; Vertex(22) = MakeVertex(1, -1, -1, 0, -1, 0, 1, 0)<br>
&nbsp;&nbsp;&nbsp; Vertex(23) = MakeVertex(-1, -1, 1, 0, -1, 0, 0, 1)<br>
&nbsp;&nbsp;&nbsp; Vertex(24) = MakeVertex(1, -1, 1, 0, -1, 0, 1, 1)<br>
<br>
<font color="#008000">&nbsp;&nbsp;&nbsp; ' Copy the vertices into the vertex buffer<br>
</font>  D3DVertexBuffer8SetData VertexBuffer, 0, 24 * Len(Vertex(1)), 0, Vertex(1)<br>
<br>
<font color="#008000">&nbsp;&nbsp;&nbsp; ' Make a list which tells the order in which to render these vertices<br>
</font>&nbsp;&nbsp;&nbsp; MakeIndices 1, 2, 3, 3, 2, 4, 5, 6, 7, 7, 6, 8, 9, 10, 11, 11, 10, 12, 13, 14, 15, 15, 14, 16, 17, 18, 19, 19, 18, 20, 21, 22, 23, 23, 22, 24<br>
<br>
<font color="#008000">&nbsp;&nbsp;&nbsp; ' Copy the indices into the index buffer<br>
</font>&nbsp;&nbsp;&nbsp; D3DIndexBuffer8SetData IndexBuffer, 0, 36 * Len(Index(1)), 0, Index(1)<br>
<br>
<font color="#008000">&nbsp;&nbsp;&nbsp; ' Set the vertex format<br>
</font>&nbsp;&nbsp;&nbsp; D3Ddevice.SetVertexShader D3DFVF_VERTEX<br>
<br>
<font color="#008000">&nbsp;&nbsp;&nbsp; ' Set the vertex and index buffers as current ones to render from<br>
</font>&nbsp;&nbsp;&nbsp; D3Ddevice.SetStreamSource 0, VertexBuffer, Len(Vertex(1))<br>
&nbsp;&nbsp;&nbsp; D3Ddevice.SetIndices IndexBuffer, -1<br>
<br>
<font color="#008000">&nbsp;&nbsp;&nbsp; ' Initializtion is complete!<br>
</font>&nbsp;&nbsp;&nbsp; Init = True<br>
&nbsp;&nbsp;&nbsp; Exit Function<br>
<br>
InitFailed: <font color="#008000"> ' the initialization function has failed</font><br>
&nbsp;&nbsp;&nbsp; Init = False<br>
<br>
End Function<br>
<br>
<br>
<br>
<br>
<br>
<font color="#008000">' MAKEVECTOR<br>
</font><br>
<font color="#008000">' This function creates vectors<br>
</font><br>
Function MakeVector(x As Single, y As Single, z As Single) As D3DVECTOR<br>
&nbsp;&nbsp;&nbsp; With MakeVector<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; .x = x<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; .y = y<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; .z = z<br>
&nbsp;&nbsp;&nbsp; End With<br>
End Function<br>
<br>
<br>
<br>
<br>
<br>
<font color="#008000">' MAKEVERTEX<br>
<br>
' This function creates vertices<br>
</font><br>
Function MakeVertex(x As Single, y As Single, z As Single, nx As Single, ny As Single, nz As Single, tu As Single, tv As Single) As D3DVERTEX<br>
&nbsp;&nbsp;&nbsp; With MakeVertex<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; .x = x<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; .y = y<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; .z = z<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; .nx = nx<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; .ny = ny<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; .nz = nz<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; .tu = tu<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; .tv = tv<br>
&nbsp;&nbsp;&nbsp; End With<br>
End Function<br>
<br>
<br>
<br>
<br>
<br>
<font color="#008000">' MAKEINDICES<br>
<br>
' This function creates a list of indices<br>
</font><br>
Function MakeIndices(ParamArray Indices()) As Integer()<br>
&nbsp;&nbsp;&nbsp; Dim i As Integer<br>
&nbsp;&nbsp;&nbsp; For i = LBound(Indices) To UBound(Indices)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Index(i + 1) = Indices(i)<br>
&nbsp;&nbsp;&nbsp; Next<br>
End Function<br>
<br>
<br>
<br>
<br>
<br>
<font color="#008000">' MAINLOOP<br>
<br>
' This sub animates the scene by moving the positions of the<br>
' cubes and the camera position, then renders the cubes. It<br>
' checks to see if the escape key has been pressed and loops<br>
' if it has not.<br>
</font><br>
Sub MainLoop()<br>
<font color="#008000">' the mathematical constant pi<br>
</font>Const PI = 3.1415<br>
<font color="#008000">' the speed of animation<br>
</font>Const SPEED = 0.01<br>
' matrices for animation and cameras<br>
Dim matTranslation As D3DMATRIX, matRotation As D3DMATRIX, matScaling As D3DMATRIX, matView As D3DMATRIX, matProjection As D3DMATRIX, matTransform As D3DMATRIX<br>
<font color="#008000">' camera position<br>
</font>Dim CameraPos As D3DVECTOR<br>
On Error Resume Next<br>
&nbsp;&nbsp;&nbsp; Do<br>
<font color="#008000">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ' let Windows messages be executed<br>
</font>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; DoEvents<br>
<font color="#008000">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ' get keyboard and mouse data<br>
</font>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Keyboard.GetDeviceStateKeyboard KeyboardState<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Mouse.GetDeviceStateMouse MouseState<br>
<font color="#008000">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ' if escape was pressed, exit program<br>
</font>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; If KeyboardState.Key(DIK_ESCAPE) Then Exit Do<br>
<font color="#008000">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ' move camera with mouse<br>
</font>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; CameraPos.y = CameraPos.y + MouseState.lY / 10<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; CameraPos.z = -2<br>
<font color="#008000">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ' set camera position, using mouse data<br>
</font>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; D3DXMatrixLookAtLH matView, MakeVector(CameraPos.x, CameraPos.y, CameraPos.z), MakeVector(0, 0, 0), MakeVector(0, 1, 0)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; D3Ddevice.SetTransform D3DTS_VIEW, matView<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; D3DXMatrixPerspectiveFovLH matProjection, PI / 3, 0.75, 0.1, 10000<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; D3Ddevice.SetTransform D3DTS_PROJECTION, matProjection<br>
<font color="#008000">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ' move the rotation angle<br>
</font>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Rotation = Rotation + SPEED<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; If Rotation > 2 * PI Then<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Rotation = Rotation - 2 * PI<br>
<font color="#008000">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
' once per rotation, play a sound<br>
</font>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Sound.Play DSBPLAY_DEFAULT<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; End If<br>
<font color="#008000">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ' clear the rendering device backbuffer and z-buffer<br>
</font>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; D3Ddevice.Clear 0, ByVal 0, D3DCLEAR_TARGET Or D3DCLEAR_ZBUFFER, vbWhite, 1#, 0<br>
<font color="#008000">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ' start rendering<br>
</font>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; D3Ddevice.BeginScene<br>
<font color="#008000">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ' create rotation matrix<br>
</font>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; D3DXMatrixRotationYawPitchRoll matTransform, Rotation * 2, Rotation, Rotation<br>
<font color="#008000">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ' set the world matrix to normal<br>
</font>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; D3Ddevice.SetTransform D3DTS_WORLD, matTransform<br>
<font color="#008000">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ' draw the medium cube<br>
</font>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; DrawCube<br>
<font color="#008000">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ' create movement, rotation and scale matrices<br>
</font>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; D3DXMatrixTranslation matTranslation, 0, 0, 4<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; D3DXMatrixRotationYawPitchRoll matRotation, 0, Rotation * 2, Rotation * 4<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; D3DXMatrixScaling matScaling, 0.5, 0.5, 0.5<br>
<font color="#008000">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ' combine them<br>
</font>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; D3DXMatrixMultiply matTransform, matRotation, matTranslation<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; D3DXMatrixMultiply matTransform, matTransform, matScaling<br>
<font color="#008000">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ' transform the world matrix<br>
</font>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; D3Ddevice.MultiplyTransform D3DTS_WORLD, matTransform<br>
<font color="#008000">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ' draw the small cube<br>
</font>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; DrawCube<br>
<font color="#008000">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ' create movement, rotation and scale matrices<br>
</font>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; D3DXMatrixTranslation matTranslation, -3, -3, -3<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; D3DXMatrixRotationYawPitchRoll matRotation, Rotation * 8, 0, Rotation * 6<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; D3DXMatrixScaling matScaling, 0.5, 0.5, 0.5<br>
<font color="#008000">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ' combine them<br>
</font>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; D3DXMatrixMultiply matTransform, matTranslation, matRotation<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; D3DXMatrixMultiply matTransform, matTransform, matScaling<br>
<font color="#008000">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ' transform the world matrix<br>
</font>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; D3Ddevice.MultiplyTransform D3DTS_WORLD, matTransform<br>
<font color="#008000">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ' draw the small cube<br>
</font>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; DrawCube<br>
<font color="#008000">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ' end rendering<br>
</font>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; D3Ddevice.EndScene<br>
<font color="#008000">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ' present the contents of the backbuffer by flipping it to the screen<br>
</font>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; D3Ddevice.Present ByVal 0, ByVal 0, 0, ByVal 0<br>
&nbsp;&nbsp;&nbsp; Loop<br>
End Sub<br>
<br>
<br>
<br>
<br>
<br>
<font color="#008000">' DRAWCUBE<br>
<br>
' Draws the cube<br>
</font><br>
Sub DrawCube()<br>
On Error Resume Next<br>
<font color="#008000">&nbsp;&nbsp;&nbsp; ' draw 12 triangles, in a cube shape, onto the backbuffer of the rendering device<br>
</font>&nbsp;&nbsp;&nbsp; D3Ddevice.DrawIndexedPrimitive D3DPT_TRIANGLELIST, 0, 36, 0, 12<br>
End Sub<br>
<br>
<br>
<br>
<br>
<font color="#008000">' CLEANUP<br>
<br>
' This unloads all the DirectX objects - we destroy objects we<br>
' have created, an disassociate our pointers from objects<br>
' create by DirectX, so then DirectX can destroy them. Failing<br>
' to call this sub can cause memory to be lost.<br>
</font><br>
Sub CleanUp()<br>
<br>
On Error Resume Next<br>
<br>
&nbsp;&nbsp;&nbsp; Set Keyboard = Nothing<br>
&nbsp;&nbsp;&nbsp; Set Mouse = Nothing<br>
&nbsp;&nbsp;&nbsp; Set DI = Nothing<br>
<br>
&nbsp;&nbsp;&nbsp; Set Sound = Nothing<br>
&nbsp;&nbsp;&nbsp; Set DS = Nothing<br>
<br>
&nbsp;&nbsp;&nbsp; Set Texture = Nothing<br>
&nbsp;&nbsp;&nbsp; Set D3Ddevice = Nothing<br>
&nbsp;&nbsp;&nbsp; Set D3DX = Nothing<br>
&nbsp;&nbsp;&nbsp; Set D3D = Nothing<br>
<br>
End Sub</p>
<p><br>
</p>
<p>---***---SOURCE CODE ENDS HERE---***---</p>
<p>Hey - does somebody have a HTML VB syntax color highlighter? As you can see,
I got fed up and didn't color in the keywords!</p>
<h4>What you have learnt</h4>
<ul>
 <li>Initialization - getting DirectX objects - loading textures, sounds,
  geometry, vertex and index buffers, getting input devices</li>
 <li>Rendering - How to draw and present texture mapped triangles</li>
 <li>Sound - erm, how to play one</li>
 <li>Input - how to read the keyboard and mouse</li>
 <li>Animation - how to use matrices to perform complex animation</li>
 <li>Alot of keywords and terms</li>
</ul>
<h4>What you should do next</h4>
<ul>
 <li>I've left a bug in the program for you on purpose! One face of each cube
  is not rendered! Find the bug and kill it! I do know the answer, honestly,
  but I'm not telling because debugging is a major part of programming for you
  to learn!</li>
 <li>Try some different shapes, animation, colors, textures, sounds, camera
  movements</li>
 <li>Try adding a background</li>
 <li>Make the program more interactive, maybe even make a puzzle or game</li>
 <li>See some of my other programs on my website for more ideas</li>
</ul>
<h4>Future Tutorials</h4>
<p>There's still lots more to learn and more advanced tutorials will come when I
get the time. Some major topics include 3D sound, lighting, and loading model
files. Give me some feedback on what you need to know.</p>
<h4>What I'd like you to do now</h4>
<ul>
 <li>Visit my website : <a href="http://www.VBgames.co.uk">www.VBgames.co.uk</a>
  - and if you have your own programming site please swap links with me</li>
 <li>Please vote for me - on <a href="http://www.planet-source-code.com">www.planet-source-code.com</a>&nbsp;</li>
 <li>Give me some feedback - go to <a href="http://www.planet-source-code.com">www.planet-source-code.com</a>
  and tell me what was good and what was bad, suggestions, comments, anything.
  Tell me why you voted the rating that you did.</li>
 <li>Hey, my request to write a book got turned down! (erm, private joke with
  someone)</li>
</ul>
<h4>Credits</h4>
<p>There are lots of sources from where my information came from. Mainly
Microsoft's DirectX SDK (as much as I hate them, DirectX rules!). Many tutorials
on <a href="http://www.planet-source-code.com">www.planet-source-code.com</a>
and <a href="http://www.gamedev.net">www.gamedev.net</a> , and also thanks to
Richard Hayden for his example program.</p>
<h4>Disclaimer</h4>
<p>This tutorial might be totally wrong so it's not my fault if something goes
wrong. You've been warned (right at the end, after you messed up your PC)!</p>
<p>&nbsp;</p>

