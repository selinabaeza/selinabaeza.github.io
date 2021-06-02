---
title: "Simulating vestibular afferent firing using a conductance-based model"
excerpt: "How do diverse sodium currents impact excitability? <br/><img src='/images/HHmodel.png'>"
collection: portfolio
---

For an explanation of the Hodgkin and Huxley formulation of sodium conductance, see [this sweet and simple summary](/files/Modeling the sodium conductance.pdf)

Hight and Kalluri (2016) published a conductance-based model of VGN firing, which was later expanded in Ventura and Kalluri (2019) to include hyperpolarization-activated cyclic nucleotide–gated (HCN) currents. They observed that VGN firing could be modulated through the low-voltage activated potassium currents (IKL). These have proved key in driving irregularity in spiking. By balancing sodium currents (INa) with IKL, they could reproduce all the VGN firing patterns and spiking seen in vivo.

<br/><img src='/images/Model spiking.png'>

Sodium currents are notoriously difficult to record in vitro. They are fast, large, and get obscured by high- and low-voltage activated potassium currents. On top of that, there is no way to pharmacologically isolate transient currents from persistent and resurgent ones. Most of our recording conditions, where we can record pure sodium currents, are extremely restricted. In conditions where we can record spiking, we cannot determine the impact of different current components in vitro. Therefore, we turned to computational methods to investigate the specific roles of these diverse currents. We have added to the VGN model (thanks for the original code base Radha!) and expanded to include resurgent and persistent sodium current components, using pseudo-HH formulation as was developed by Venugopal et al., 2018.

<br/><img src='/images/modelings eqs.png'><br/>

Using data from our electrophysiology as parameters, we can use these to reproduce the kinetics and voltage dependence of all three current components. With these additions, we have been investigating the influences that each individual current component has on step-evoked firing and EPSC-evoked firing. We are testing the impact on current threshold, firing threshold, spike latency, and response range - all of which are measures of excitability. Stay tuned. 

<img src='/images/Manuscript_fig_1D.png'>

****Literature Cited****

- Hight AE, Kalluri R. A biophysical model examining the role of low-voltage-activated potassium currents in shaping the responses of vestibular ganglion neurons. Journal of Neurophysiology 116: 503–521, 2016.
- Hodgkin AL, Huxley AF. A quantitative description of membrane current and its application to conduction and excitation in nerve. The Journal of Physiology 117: 500–544, 1952.
- Kalluri R, Xue J, Eatock RA. Ion Channels Set Spike Timing Regularity of Mammalian Vestibular Afferent Neurons. Journal of Neurophysiology 104: 2034–2051, 2010.
- Khaliq ZM, Gouwens NW, Raman IM. The Contribution of Resurgent Sodium Current to High-Frequency Firing in Purkinje Neurons: An Experimental and Modeling Study. J Neurosci 23: 4899–4912, 2003.
- Rothman JS, Manis PB. The Roles Potassium Currents Play in Regulating the Electrical Activity of Ventral Cochlear Nucleus Neurons. Journal of Neurophysiology 89: 3097–3113, 2003.
- Ventura CM, Kalluri R. Enhanced Activation of HCN Channels Reduces Excitability and Spike-Timing Regularity in Maturing Vestibular Afferent Neurons. J Neurosci 39: 2860–2876, 2019.
- Venugopal S, Seki S, Terman DH, Pantazis A, Olcese R, Wiedau-Pazos M, Chandler SH. Resurgent Na+ Current Offers Noise Modulation in Bursting Neurons. PLOS Computational Biology 15: e1007154, 2019.


