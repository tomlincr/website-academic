---
title: Wearables for Home Post-Operative Monitoring: Proof of Concept
author: admin
date: '2020-06-27'
tags:
  - poster
  - perioperative medicine
  - anaesthesia
event: EBPOM 2020 Annual London Congress of Perioperative Medicine
event_url: https://ebpom.org
location: Online
address:
  street: ~
  city: ~
  region: ~
  postcode: ~
  country: ~
summary: ~
abstract: ~
date_end: ''
all_day: no
publishDate: '2020-06-27'
authors: [C Tomlinson]
featured: no
image:
  caption: ''
  focal_point: ''
  preview_only: no
doi: http://dx.doi.org/10.13140/RG.2.2.11804.72328
url_slides: ~
url_source: https://dcs.mediazoom.org/sites/23/2020/09/10202103/EBPOM-LONDON-2020-Abstract-Competition.pdf
url_pdf: https://www.researchgate.net/publication/342492471_Wearables_for_Home_Post-Operative_Monitoring_Proof_of_Concept
url_code: https://ctomlinson.net/tag/EBPOM2020/ 
slides: ''
projects: []
---

We hypothesise that wearables could transform perioperative care, including through facilitating early-discharge, a key tenant of Enhanced Recovery After Surgery (ERAS), by enabling remote patient monitoring of physiological & functional variables.

Utilising a commercially available fitness tracker (Charge 4, Fitbit ®) and Application Program Interface (API) it was possible to import measured data into R for further statistical computation. Both physiological (heart rate (HR)) and functional (sleep duration, step count) variables were accessible. Whilst the device includes a pulse oximeter, this is unavailable via the API. Owing to COVID-19 this methodology was trialled on a volunteer and serves only as proof of concept.

Once can easily ‘eyeball’ a resting HR of ~53, a peak of ~145 during exercise and that HR was generally within normal limits on the NEWS2 score. They undertook two periods of exercise, lasting ~90 & ~60 mins, respectively, and slept for ~7.5 hours, with little disturbance.

From the recorded parameters we may expect to see patterns of abnormalities consistent with post-operative complications, for example pain illustrated by a tachycardia and reduction in activity and sleep (Table 1). This could be greatly enhanced with SpO2, via an API update.


Other methods of outlier detection could include reference ranges (e.g. NEWS2 – visualised in Figure 1) or comparison with peers (e.g. 95th centiles). Following identification this may prompt increased follow-up, e.g. telephone call or ‘push-notification’ to patient outcome reporting app.

Furthermore, captured data contributes to a core & extended perioperative outcome set (Myles et al., 2016) for further high-quality research.

Remote patient monitoring, via wearable fitness trackers, is achievable and has potential to provide meaningful benefit, by facilitating early discharge and detection of complications, as part of an ERAS pathway. Following proof of concept we hope to trial this tool clinically.

References

Royal College of Physicians. National Early Warning Score (NEWS) 2 Standardising the assessment of acute-illness severity in the NHS. Updated report of a working party. London RCP, 2017.

P. S. Myles, M. P. W. Grocott, O. Boney, S. R. Moonesinghe, on behalf of the COMPAC-StEP Group, Paul Myles, Michael Grocott, Bruce Biccard, Oliver Boney, Matthew Chan, Lee Fleisher, Cor Kalkman, Andrea Kurz, Ramani Moonesinghe, Duminda Wijeysundera, J. Bartoszko, W. S. Beattie, R. Bellomo, D. Buggy, L. Cabrini, J. Canet, T. Cook, D. J. Cooper, T. Corcoran, P. J. Devereaux, R. Eckenhoff, L. Evered, T. J. Gan, T. Gin, H. Grocott, G. Haller, S. Howell, M. Jayarajah, C. Kalkman, K. Karkouti, B. Kavanagh, A. Klein, G. Landoni, K. Leslie, D. R. McIlroy, D. Mazer, A. Moller, M. Mythen, M. Neuman, M. Neuman, R. Pearse, P. Peyton, J. Prowle, T. Richards, D. A. Scott, D. Sessler, A. Shaw, T. Short, M. Shulman, B. Silbert, M. Singer, J. R. Sneyd, D. Story, D. van Dijk, W. van Klei, on behalf of the COMPAC-StEP Group, Standardizing end points in perioperative trials towards a core and extended outcome set, BJA British Journal of Anaesthesia, Volume 116, Issue 5, May 2016, Pages 586–589, <https://doi.org/10.1093/bja/aew066>

R code for data import & analysis freely available at <https://ctomlinson.net/tag/EBPOM2020/>