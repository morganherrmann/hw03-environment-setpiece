# CIS 566 Homework 3: Environment Setpiece

### Golden Fantasy Forest
Morgan Herrmann
moher@seas.upenn.edu

## Assignment Requirements
#### Animation of the camera or environment elements
The glitter-tree leaves are animated with respect to time.  Lighting fog color and fog strength also vary with time.
#### Three different uses of noise (for color, shape, normal, glow, etc.)
- iChannel Shadertoy input noise was used to create the base height for the ground.
- FBM was used to compute the coloring of the ground, by setting a threshhold for red and yellow splotches.
- FBM was also used to compute the striations for the gold appearance of the well.  By using Blinn Phong shading and using noise based on the x and z value, I was able to create reflectivity that looks like gold.
- Noise was also used to vary the width of the individual trees!
#### Remapping of a value [0, 1] to a set of colors
- The color of the fog uses mix and cosine curve values to map a value from [0,1] (in this case, using variations of sin(Time)) to a color pallette that alternates between greyish red, greyish yellow, and greyish blues. This color mapping can be observed in the fog changing colors in the background.

#### ToolBox Functions
Many sin displacement functions were used within the trees, as well as smoothsteps between colors.

#### Approximated environmental lighting using three to four directional lights and ambient light
3 Directional and ambient light was used to mimic a dusty, hazy forest made of gold.
Some of the lighting also shifts with respect to time to add more life to the sene.

#### SDF-based soft shadows
SDF based soft shadows are used to make the scene feel more realistic.  
Source for implementing: http://iquilezles.org/www/articles/rmshadows/rmshadows.htm

#### Additional Elements
  - Color remapping - Color remapping is previously mentioned above, as used for the distance fog.
  - SDF blending - SDF blending was used to combine basic cylinders, capsules, and other shapes into the golden well, and the trees as well.
  - Distance fog - Distance fog was implemented according to http://iquilezles.org/www/articles/fog/fog.htm , and was utilized to make the forest feel more mystical and mysterious.






