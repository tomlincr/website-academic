---
title: 'Foresight: a generative AI model of patient trajectories across the COVID-19 pandemic'
summary: "Developing the first national-scale generative AI model of electronic health records.."
tags:
- Risk prediction
- Machine learning
- Deep learning
- EHR
- Transformers
- Generative AI
- 'NHS Secure Data Environment'
- Industry collaboration

date: "2023-12-23"

# Optional external URL for project (replaces project detail page).
external_link: ~
links:
url_code: ""
url_pdf: ""
url_slides: ""
url_video: ""

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""
---

📣 We are developing Foresight - the first national-scale generative AI model of electronic health records.

💡 Foresight is about bringing the latest advances in AI, behind models like chatGPT, to healthcare data. Instead of predicting the next word in a sentence, Foresight predicts a person's next healthcare event, based on their previous medical history.

🔮 As a foundation model, Foresight is a single model, capable of making predictions across the full spectrum of a person’s health, unlocking exciting possibilities across healthcare and research.

🤝 Through an innovative academic-industry-NHS partnership we have brought the compute required to train AI inside the NHS England Secure Data Environment for the first time.

📈 Allows us to scale earlier work ([Zeljko Kraljevic et al. in Lancet Digital Health 2024](https://doi.org/10.1016/S2589-7500(24)00025-6)) up to 57M patients, approximately the population of England.

💡 This scale is crucial. AI models are only as good as the data on which they’re trained. If we want a model that can benefit all patients, with all conditions, then the AI needs to have seen that during training. 

🌈 Using national-scale data allows us to represent the kaleidoscopic diversity of England’s population, particularly for minority groups and rare diseases, which are often excluded from research.

This is currently a pilot research study, we’re at the point of rigorously evaluating the model:  
🦠 We’re looking at predicting COVID-19 outcomes. 
🚀 We’re also testing the models ability to ‘generalise’ to other important healthcare outcomes: such as predicting the risk of hospitalisation or death in the next year, as well as the onset of over a thousand different conditions.  
🔎 That rigorous evaluation will include looking at algorithmic bias, which public and patient contributors who’ve shaped our research have emphasised the importance of.  

💡 The take home message here is that Foresight is a single ‘foundation’ model, capable of predicting the full range of healthcare events it’s seen during training. 

We would like to see that broad potential converted into benefit, we’re approaching this through:  
🎓 Collaborating with other approved researchers in the CVD-COVID-UK consortium to let them scrutinise Foresight and understand how it can support their research.  
🔓 Exploring how to responsibly expand the scope of the model, which is currently restricted to COVID-related research.  
🩻 Increase the depth and capability of Foresight by including richer sources of information like clinicians’ notes, or results of investigations such as blood tests and scans. These data aren’t currently available at national-scale.  

Ultimately we believe Foresight is an exciting step towards being able to predict disease and complications before they happen, giving us a window to intervene and enabling a shift towards more preventative healthcare at scale.

## Government and NHS support

Health and Social Care Secretary Wes Streeting said:  
> Our Plan for Change is harnessing trailblazing AI to radically transform our NHS – while also protecting patient data with strict security procedures. I’m determined that we use this kind of groundbreaking technology to cut down on unnecessary hospital trips, speed up diagnosis times, and free up staff time. AI will be central as we bring our analogue NHS into the digital age to deliver faster and smarter care across the country.  

Science and Technology Secretary Peter Kyle said:  
> This ambitious research shows how AI, paired with the NHS’s wealth of secure and anonymised data, is set to unlock a healthcare revolution. This technology is transforming what’s possible in tackling a host of debilitating diseases, from diagnosis, to treatment, to prevention. This is work that that will be instrumental to this Government’s missions to overhaul healthcare and grow the economy, which sit at the heart of our Plan for Change. And an unrelenting focus on privacy and security, means people can rest assured that their data is in safe hands.  

Dr Vin Diwakar, National Director of Transformation at NHS England, said:  
> AI has the potential to transform the way we prevent and treat disease, if trained on large datasets and safely tested. The NHS Secure Data Environment has been fundamental to this pioneering research, shaping a future where earlier treatments and interventions are targeted to those who will benefit, preventing future ill health. This will boost our ability to move quickly towards personalised, preventative care.  

Chief Scientific Advisor for the Department of Health and Social Care Lucy Chappell said:  
> Using AI to drive innovation across the NHS is key in making strides for better care to patients. This study could allow earlier diagnosis and treatment, enabling people to better manage their health and care, whilst ensuring patient data is safeguarded. The NIHR is proud to be supporting this work through our world-leading infrastructure.  

## Partners

Foresight is a collaboration between NHS England, UCL, King’s College London, National Institute for Health and Care Research Biomedical Research Centres (University College London Hospital, Maudsley), NHS Foundation Trusts (King’s College Hospital, South London and Maudsley), British Heart Foundation Data Science Centre’s CVD-COVID-UK/COVID-IMPACT Consortium, and technology partners AWS, Databricks, and CogStack.  

Funders and oversight bodies include NHS AI Lab, UK Research and Innovation, Medical Research Council, National Institute for Health and Care Research, and Health Data Research UK.  

Industry partners like Amazon Web Services (AWS) and Databricks support with computational resources but can't access NHS data, the AI model, or its outputs. They have no control over the research or its findings.  

## Further information

### Official press releases

* [AI model trained on de-identified data from 57 million people](https://www.ucl.ac.uk/news/2025/may/ai-model-trained-de-identified-data-57-million-people). UCL News. 07/06/2025.
* [Groundbreaking AI trained on de-identified patient data to predict healthcare needs](https://bhfdatasciencecentre.org/news-and-events/groundbreaking-ai-trained-on-de-identified-patient-data-to-predict-healthcare-needs/). British Heart Foundation Data Science Centre. 07/06/2025.
* [Groundbreaking AI trained on de-identified patient data to predict healthcare needs](https://www.uclhospitals.brc.nihr.ac.uk/news/groundbreaking-ai-trained-de-identified-patient-data-predict-healthcare-needs). NIHR UCLH Biomedical Research Centre. 07/06/2025.
*   [Groundbreaking AI trained on de-identified patient data to predict healthcare needs](https://www.kcl.ac.uk/news/ai-to-predict-healthcare-needs). King's College London. 07/06/2025.

### Official information

* [Project Summary: CCU078: Foresight: a generative AI model of patient trajectories across the COVID-19 pandemic](https://bhfdatasciencecentre.org/projects/ccu078/) British Heart Foundation Data Science Centre.  
* [Research powered by data: Foresight AI case study](https://digital.nhs.uk/data-and-information/research-powered-by-data/case-studies/foresight-ai). NHS England.  

### Media coverage

* [New AI tool could help NHS predict who will fall ill in 'healthcare revolution'](https://www.mirror.co.uk/news/uk-news/new-ai-tool-could-help-35180448). Martin Bagot, The Mirror. 07/06/2025.  
* [AI to predict future illnesses using NHS patient data](https://www.telegraph.co.uk/news/2025/05/07/ai-will-predict-future-illness-by-analysing-nhs-data/). Michael Searles, The Telegraph (Paywalled). 07/06/2025.  
* [New AI model uses NHS data to predict future disease and complications](https://www.independent.co.uk/news/health/nhs-uk-data-ai-model-foresight-disease-b2746646.html). Storm Newton, PA for The Independent. 07/06/2025.  
* [AI model being trained with NHS data from 57m people ‘could predict disease’](https://www.standard.co.uk/news/tech/nhs-england-peter-kyle-ucl-university-college-london-b1226248.html). Storm Newton, PA for The Standard. 07/06/2025.  
* [Medical AI trained on whopping 57 million health records](https://www.nature.com/articles/d41586-025-01422-3). Ewen Callaway, Nature News (Paywalled). 07/06/2025.  
* [Expert reaction to the development of a generative AI model trained on de-identified NHS patient data to predict healthcare needs](https://www.sciencemediacentre.org/expert-reaction-to-the-development-of-a-generative-ai-model-trained-on-de-identified-nhs-patient-data-to-predict-healthcare-needs/). Science Media Centre. 07/06/2025.  
