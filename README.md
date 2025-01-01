## PhaseDemo
A collection of assets to create animated (via scrolling phase) simulations of wave interference and diffraction in VRChat.
The wave simulations utilise a technique that involves scrolling the phase of a wave field to provide the illusion of wave motion, hence the name "PhaseDemo".

# Prerequisite packages:
Begin a new VRChat world project with VRCW Foundation selected, and once loaded into the editor, install the TextmeshPro (Essentials) package from the package manager. 

# Usage
Clone the repository code and copy it to the project's assets folder.

Once the project's assets are imported, three scenes should be available:

- BasicWavePanel: This contains an example of the 'trippy' wave interference panel as used in some of my worlds. The simulation uses a custom render texture to calculate a wave interference pattern's real and imaginary components in a single pass. The output texture is then displayed by a custom fragment shader that scrolls the phase to provide the illusion of wave motion.
- BasicParticleDemo: This simulation comprises two overlaid quantum scattering simulations generated from the same quantum scattering model.
  1. A particle scattering simulation that operates in two modes, pulsed and continuous.
  2. A probability density overlay.
   
