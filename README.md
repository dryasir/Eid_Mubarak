# Eid Mubarak
__Dr. Yasir Bashir__
Geoscienitst & Professor at Istanbul Technical University, Turkey

This repository presents a Python-based workflow for generating a synthetic seismic section using fundamental principles of reflection seismology. The script demonstrates how to construct a reflectivity model, simulate seismic wave propagation through convolution with a wavelet, and visualize the resulting seismic data.

The code creates a 2D seismic dataset (time vs. trace) in which the words “EID MUBARAK” or "IYI BAYRAMLAR" and a signature “DYB” are embedded as high-reflectivity features. These features are then transformed into realistic seismic responses through wavelet convolution and noise addition.

⚙️ __Methodology__

The workflow follows the classical convolutional seismic model:

__1- Seismic Canvas Creation__
  
  A 2D array is initialized to represent the seismic section, with small random values simulating background geological reflectivity.
  
__2- Text-Based Reflectivity Modeling__
  
  The words are rendered using the Pillow (PIL) library and converted into a binary mask.
  
   Pixels corresponding to the text are assigned high reflectivity values.
      
   Background pixels retain low-amplitude random values.
      
__3- Wavelet Generation__
  
  A 30 Hz Ricker wavelet is generated to simulate the seismic source signature.
  
__4- Convolution (Forward Modeling)__
  
  Each trace is convolved with the wavelet to produce realistic seismic reflections, including characteristic sidelobes.
  
__5- Noise Addition__
  Gaussian noise is added to simulate real-world acquisition conditions and improve realism.
  
__6- Amplitude Normalization__
  
  The seismic amplitudes are scaled to a standard range for consistent visualization.
  
__7- Visualization__
 
  The final seismic section is displayed using a diverging colormap (e.g., RdBu), where positive and negative amplitudes represent seismic polarity.
