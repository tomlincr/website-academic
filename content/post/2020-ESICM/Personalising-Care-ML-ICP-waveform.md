---
title: "ESICM LIVES2020: Personalising Care: ML from ICP waves"
date: 2020-12-08
draft: false
featured: true
authors:
  - admin
tags:
  - ESICM
  - conference
  - LIVES2020
  - ICM
  - ML
  - waveforms
image:
  filename: ""
  focal_point: ""
  preview_only: false
---
Below you can find my notes from this talk at the ESICM LIVES 2020.  

Thanks to [Adrian Wong (@avkwong)](https://twitter.com/avkwong) for inviting me to [blog on the ESICM website where you can find the full version of the below, including some slides](https://www.esicm.org/blog/?p=3072).

---

💬 Personalising Care: Machine learning from pressure waves (ICP)  
🩺 Soojin Park, Associate Prof. Neurology  
🏥 Division of Neurocritical Care, Columbia University, NYC, USA  
📺 Watch on demand: https://lives2020.e-lives.org/media/machine-learning-pressure-waves  

---

❗ Motivation  
· Acute hydrocephalus affects ~37k pts/yr in USA  
· Rx = EVD, but 1/5th develop infection ventriculitis  
· Risk of ventriculitis ↑ with duration and frequency of CSF sampling (by which diagnosis made..)  

❓ Question  
Can we find a way of using physiological information contained in ICP waveform to develop a method for detecting ventriculitis, without having to sample CSF?

Park reminds us of the normal ICP waveform (exam revision déjà vu..)  

 And how it’s morphology changes with ↑ICP  

This alteration in waveform morphology with ↑ICP has a biologically plausible mechanism in ventriculitis.  

 ⭐ Goal 1  
Examine changes in ICP waveform morphologies prior to ventriculitis  

· Dataset = only patients WITH ventriculitis  
· Collaboration with group experienced in ICP waveform big data, however their pre-processing identified abnormal waveforms as artefactual!  
· ⚠Problem = vague definition of ventriculitis  
· Used ‘gold standard’ of limiting it to those with culture-positive CSF  
· n = 19 pts  
· ❗ Park mentions that CSF is cultured 3/w at this institution, perhaps not usual practice – CT: worth considering this in the context of their motivation  

· ⚠ EVDs left open to drainage most of the time, typical practice across other institutions, thus waveform only intermittently present when EVD clamped by nurse  
· ❓ Challenge = automating identification of waveforms (CT: I note solution was not to get desperate medical student to manually sift data in exchange for ‘research experience on their CV..)  

🔧 Methods  
· Dominant pulses extracted using Morphological Clustering Analysis of ICP Pulse  
· Before / During / After ventriculitis (i.e culture-positive CSF)  
· Morphologically similar groups obtained by hierarchical k-means clustering  
· Dynamic Time Warping used as a ‘distance’ metric to correct for speed (HR), see below  
· Meta-clusters determined by clinicians, see figure B below.  
· Bi/triphasic (green)  
· Monophasic/tombstone (yellow)  
· Artefactual (red)  
· = supervised learning  

📜 Results  
· Prior to ventriculitis majority of pulses had physiological tri/biphasic appearance  
· During ventriculitis this dropped from 61.8 > 22.6%, a statistically significant change, which persisted  
· ✨ Most importantly this change occurred a full day before the ventriculitis was clinically detectable  

  ⭐ Goal 2  
Leverage time-varying dominant pulses of ICP from hourly EVD clamping data into a detection model of ventriculitis  
· Collaboration:  
· Columbia Vangelos College of Physicians & Surgeons  
· R Adams Cowley Shock Trauma Center, University of Maryland  
· Aims:  
· Improve performance and generalisability of model to other institutions data  
· Work in submission therefore not shown  
· Collaborators sought, see email below:  

 🚩 Concluding Remarks  
· Example presented for ICP but process generalisable to other waveforms, of which there are many in ICU!  

---

🙋‍♂️ My thoughts:  
· I’ve often been disappointed at how little waveform data is actually stored from ICU monitors  
· Perhaps I shouldn’t be given the general lack of high-quality ICU data (see data sharing session) and huge storage requirements  
· Most of the ‘high resolution/granular/insert other buzzword here’ EHRs I’ve come across sample at a frequency ~ 1 hz (c.f. 125-250 hZ in this study)  
· Starting point for those interested in waveform data in ICU = MIMIC-III Waveform Database  
· Be warned this is truly *big* data!
