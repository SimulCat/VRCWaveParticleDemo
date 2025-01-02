# PhaseDemo

A collection of assets to create animated (via scrolling phase) simulations of wave interference and diffraction in VRChat.
The wave simulations use a technique involving scrolling the phase of a wave field to provide the illusion of wave motion, hence the name "PhaseDemo."

## Prerequisite packages

Begin a new VRChat world project with the VRCW Foundation package selected. Once the project is loaded in the editor, install the TextmeshPro (Essentials) package from the package manager.

## Usage

With the base project established, clone and copy the repository code to the assets folder.

Once the new assets are imported, three scenes should be available:

- BasicWavePanel: This contains an example of the 'trippy' wave interference panel as used in some of my worlds. The simulation uses a custom render texture to calculate a wave interference pattern's real and imaginary components in a single pass. The output texture is then displayed by a custom fragment shader that scrolls the phase to provide the illusion of wave motion.
  ![Simulated Double Slit Pattern](https://simulcat.github.io/blob/phasedemo/twinenergy.gif)
- BasicParticleDemo: This simulation comprises two overlaid quantum scattering simulations generated from the same quantum scattering model.
  1. A particle scattering simulation that operates in two modes, pulsed and continuous.
  2. A probability density overlay.
- DualDemo: This demonstration pairs the particle demonstration with a wave panel with matching dimensions. With Planck's constant for the particle simulation set to '1' and the wavelength for the wave simulation set to the inverse of the particle momentum, the two simulations independently produce the same scattering and energy distributions with the same aperture patterns.
