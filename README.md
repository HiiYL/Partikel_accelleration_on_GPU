# Particle-Simulation using the GPU via the OpenGL Compute-Shader

This particle simulation is more like a proof of concept for myself or others to show and understand how compute shaders in OpenGL work.
Using the knowledge I gathered from this project, more complex, fascinating and fast projects are possible, which use the power of
the GPU for computations which would normally be not possible in real time or a lot slower.

**And most important:**

With the compute-shader, I can simulate 8,000,000 independent particles in about 60fps on a GTX-660 (which is ok, but not really very good).

The final endresult looks like that:

![Particle-Simulation](https://github.com/MauriceGit/Partikel_accelleration_on_GPU/blob/master/Screenshots/screenshot_31.png "Particle-Simulation screenshot")

## **Animation**

The physics of this animation are pretty straight forward. Each particle has a life-span in which it fades from red (new born) to blue (about dying).
When a particle dies, it respawnes in its inverted (x,y,z) position.

The movement itself is computed by calculating a Euler-integration for each particle. That means a force is calculated (dependant on the distance),
then an acceleration, velocity and new position.

There is a global attraction pole which moves just random! (Pure randomness).

So the movement of the particles are just random following or moving around the attraction point.

In the following screenshots you can see the following aspect (when the attraction center moved away fast for example):

![Particle-Simulation](https://github.com/MauriceGit/Partikel_accelleration_on_GPU/blob/master/Screenshots/screenshot_13.png "Particle-Simulation screenshot")
![Particle-Simulation](https://github.com/MauriceGit/Partikel_accelleration_on_GPU/blob/master/Screenshots/screenshot_14.png "Particle-Simulation screenshot")
![Particle-Simulation](https://github.com/MauriceGit/Partikel_accelleration_on_GPU/blob/master/Screenshots/screenshot_27.png "Particle-Simulation screenshot")

## **Install && Run**

I only tested an ran this simulation on a debian-based unix OS (Ubuntu, Mint, ...). It should run on any other machine as well but is not
tested.

### **System Requirements**

The following system-attributes are required for running this simulation:

- A graphics card supporting OpenGL version 4.3 (For the compute-shader!).

- Unix-Libraries: xorg-dev and mesa-common-dev

Both GLEW (The OpenGL Extension Wrangler Library) and GLFW (Window-Manager) are now included locally, so no system wide
installation is necessary!

Anyway, just for your interest, you could get them there:

- GLFW: [http://www.glfw.org/](http://www.glfw.org/).

- GLEW (with install instructions): [http://glew.sourceforge.net/build.html](http://glew.sourceforge.net/build.html).

### **Running**

Compiling and running is then pretty straight forward.
It should also work in windows and OSX, but is not tested.
In the root directory, do:

- cmake .

- make

- cd bin/

- ./particleSim

While the simulation runs, you can move around (always looking to the center!) with your mouse (left-klick and move) and zoom in/out with your mouse (right click and move up/down).

## **More Screenshots**

So, here are some more screenshots, because screenshots are awesome :)

You can find some more screenshots in the screenshot-folder: [More Screenshots :)](https://github.com/MauriceGit/Partikel_accelleration_on_GPU/tree/master/Screenshots).

![Particle-Simulation](https://github.com/MauriceGit/Partikel_accelleration_on_GPU/blob/master/Screenshots/screenshot_35.png "Particle-Simulation screenshot")
![Particle-Simulation](https://github.com/MauriceGit/Partikel_accelleration_on_GPU/blob/master/Screenshots/screenshot_39.png "Particle-Simulation screenshot")
![Particle-Simulation](https://github.com/MauriceGit/Partikel_accelleration_on_GPU/blob/master/Screenshots/screenshot_40.png "Particle-Simulation screenshot")
![Particle-Simulation](https://github.com/MauriceGit/Partikel_accelleration_on_GPU/blob/master/Screenshots/screenshot_30.png "Particle-Simulation screenshot")
![Particle-Simulation](https://github.com/MauriceGit/Partikel_accelleration_on_GPU/blob/master/Screenshots/screenshot_0.png "Particle-Simulation screenshot")
![Particle-Simulation](https://github.com/MauriceGit/Partikel_accelleration_on_GPU/blob/master/Screenshots/screenshot_8.png "Particle-Simulation screenshot")
![Particle-Simulation](https://github.com/MauriceGit/Partikel_accelleration_on_GPU/blob/master/Screenshots/screenshot_10.png "Particle-Simulation screenshot")
![Particle-Simulation](https://github.com/MauriceGit/Partikel_accelleration_on_GPU/blob/master/Screenshots/screenshot_11.png "Particle-Simulation screenshot")
![Particle-Simulation](https://github.com/MauriceGit/Partikel_accelleration_on_GPU/blob/master/Screenshots/screenshot_22.png "Particle-Simulation screenshot")






