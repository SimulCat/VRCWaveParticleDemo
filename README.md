# VRChat Wave/Particle Demo

This repository contains a collection of assets and example scenes demonstrating how to build and recreate the wave and particle simulations used in VRChat worlds published by K_Cat (KilkennyCat).

Currently, the repository contains three pre-configured scenes: BasicParticlePanel, BasicWavePanel, and DualDemo. 
The first two scenes illustrate how to build separate particle and wave simulations; the third integrates them to demonstrate the correspondence between wave and particle scattering models side by side and as an overlay.

## Prerequisite

Begin a new VRChat world project (Unity 2022) with the VRCW Foundation package added. Once the project is loaded in the editor, install the TextmeshPro (Essentials) package from the package manager.
Open the project (it will open with the VRCHat default world scene, open the package manager and then add TextmeshPro (Just the essentials), as this is used in the demo user interface.

## Usage

With the base project established, clone, then copy the contents of the cloned repository to the assets folder. 

Once the new assets are imported, three scenes should be available:

- BasicWavePanel: This contains an example of the 'trippy' wave interference panel as used in some of my worlds. The simulation uses a custom render texture to calculate a wave interference pattern's real and imaginary components in a single pass. The output texture is then displayed by a custom fragment shader that scrolls the phase to provide the illusion of wave motion.
![Simulated Double Slit Pattern](https://github.com/SimulCat/simulcat.github.io/blob/main/phasedemo/twinenergy.gif)
- BasicParticleDemo: This simulation comprises two overlaid quantum scattering simulations generated from the same quantum scattering model.
  1. A particle scattering simulation that operates in two modes, pulsed and continuous.
  2. A probability density overlay.
- DualDemo: This demonstration pairs the particle demonstration with a wave panel with matching dimensions. With Planck's constant for the particle simulation set to '1' and the wavelength for the wave simulation set to the inverse of the particle momentum, the two simulations independently produce the same scattering and energy distributions with the same aperture patterns.
