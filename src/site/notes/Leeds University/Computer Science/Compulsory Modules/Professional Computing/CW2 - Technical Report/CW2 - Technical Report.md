---
{"dg-publish":true,"permalink":"/leeds-university/computer-science/compulsory-modules/professional-computing/cw-2-technical-report/cw-2-technical-report/"}
---

# Smart Homes, Smarter Energy: The Role of AI in Reducing Home Energy Use
~~Thomas Carey
05/12/2023
Summary: 95 words
Report: 783 words~~

---

##### Summary
Artificial Intelligence (AI) can revolutionize the way we manage and conserve energy our homes. This report explores two different approaches to AI-based Home Energy Management Systems (HEMS) and their impact on energy efficiency and carbon emissions. I analysed both real-world case study where an AI controlled heater showed a 14% reduction in energy (Kwon et al., 2022) and an advanced simulation which displayed a “reduction in the burden on the legacy grid” (Prakash N. and Vadana D., 2017). The results show that AI-based HEMS are both feasible and efficient, however, they are costly to implement.

## Introduction
In recent years AI has become much more prevalent in our personal lives. With the invention of tools such as the Google Assistant and Amazon Alexa along with the widespread integration of the Internet of Things (IoT) our houses are becoming more automated by the day.
My objective in this report is to explore how AI is currently used in homes, how effective these AIs are at reducing energy consumption and how comfortable the general public feels about AI managing their homes energy. I also plan to include any thoughts I have on how the current methods could be improved.
## Review of Existing Research
In this report, I conducted a review of academic papers using the OpenAI Bing Chat model to locate relevant studies. The search strategy involved the use of keywords such as ‘net-zero’, ‘smart home’, ‘AI’ and ‘EMS’ (Energy Management System). My inclusion criteria focused on studies that were in English and had a focus on energy management in a residential setting.
My research found me two important studies where they both developed different approaches to the issue. Kwon et al.’s (2022) AI-based HEMS (Home Energy Management System) uses AI to control the heater efficiently, and Prakash N. and Vadana D.’s (2017) Intelligent REMS (Residential Energy Management System) controls a personal renewable energy source.

### AI-HEMS
Kwon et al. (2022) proposed an AI-based HEMS (AI-HEMS) that monitors a house and it’s occupants, such as when they leave, when they sleep and which rooms are currently occupied. The AI-HEMS used this data to intelligently control a heater and through a performance analysis, was found to reduce *absolute* energy consumption by 14%, definitely reducing the carbon footprint. Since the test was carried out without dynamic electricity pricing, assuming that heating bills are calculated in proportion to energy savings, it can be said that there was also an approximate 14% reduction in heating bills (Kwon et al., 2022).
This shows an apparent improvement over Google Nest, the current state-of-the-art AI-thermostat, which saves an average of 10%–12% on heating bills (Google, n.d.). However, the US follows dynamic energy pricing so this cannot be equated to energy savings or a reduction in carbon footprint. Furthermore, after the analysis a survey found resident satisfaction with the AI-HEMS to be approximately 91% (Kwon et al., 2022).
### IREMS
Prakash N. and Vadana D. (2017) proposed a different system, one they called an Intelligent Residential Energy Management System (IREMS). This system works by regularly monitoring the status of the building and choosing from 4 different decisions, as shown in [[Leeds University/Computer Science/Compulsory Modules/Professional Computing/CW2 - Technical Report/CW2 - Technical Report#^Table-I\|Table I]].

| Decisions | Description |
| :-: | :- | 
| 1 | Maintain the same state |
| 2 | Redirect to Battery |
| 3 | Redirect to Grid |
| 4 | Message Consumer |
{ #Table-I}


<figcaption>Table I. Decisions</figcaption>

The IREMS was designed for a building with its own source of renewable energy, such as a solar panel, hence the battery. Contrary to the AI-HEMS this system does not directly turn off any devices, only warns the consumer they are using too much energy (Prakash N. and Vadana D., 2017).
The IREMS was simulated using two different intelligent algorithms, namely an Artificial Neural Network (ANN) and a Support Vector Machine (SVM). Through rigorous testing, they found that SVM had superior accuracy (Prakash N. and Vadana D., 2017).

“REMS when installed in every home cumulatively show a significant reduction in the burden on the legacy grid and improvement in the small scale penetration of renewable energy resources.” (Prakash N. and Vadana D., 2017)
## Conclusions
These results show that using AI controlled energy management systems are a feasible method to lead towards a net-zero society. The two approaches show both reducing carbon footprint, through lower energy consumption and using renewable energy in Prakash N. and Vadana D.’s (2017) case. Furthermore, both studies preserve the comfort of the user with not directly effecting it by switching back and forth from battery.
While both proposals show promise, I believe they could be combined to provide greater results. For example, in Prakash N. and Vadana D.’s (2017) study they found that an SVM algorithm was more accurate with its decisions than an ANN, which is what Kwon et al. (2022) used. Also, instead of the ‘Message consumer’ (Prakash N. and Vadana D., 2017) decision, they could instead implement the design of Kwon et al.’s (2022) AI-HEMS and automatically adjust what is taking energy to reduce manual intervention.
The main barriers to both of these energy management systems (EMS) are the upfront costs. Both require devices in each room, with Kwon et al.’s (2022) requiring various different sensors and Prakash N. and Vadana D.’s (2017) needing controllers as well as source of renewable energy and a battery to store it.
In conclusion I believe AI based EMSs are both practical and a good investment to saving energy, but would require monetary support to become widespread due to their expensive cost to implement.

---
## References

Kwon, K., Lee, S. and Kim, S. 2022. AI-Based Home Energy Management System Considering Energy Efficiency and Resident Satisfaction. _IEEE Internet of Things Journal_. **9**(2), pp.1608–1621.

Mahapatra, B. and Nayyar, A. 2022. Home energy management system (HEMS): concept, architecture, infrastructure, challenges and energy management schemes. _Energy Systems_. **13**(3), pp.643–669.

Prakash N., K. and Vadana D., P. 2017. Machine Learning Based Residential Energy Management System _In_: _2017 IEEE International Conference on Computational Intelligence and Computing Research (ICCIC)_ [Online]., pp.1–4. [Accessed 4 December 2023]. Available from: [https://ieeexplore.ieee.org/document/8524383](https://ieeexplore.ieee.org/document/8524383).

Google n.d. Save energy and live comfortably with Nest thermostat savings. _Google Store_. [Online]. [Accessed 3 December 2023]. Available from: [https://store.google.com/intl/en/ideas/articles/nest-thermostat-savings/](https://store.google.com/intl/en/ideas/articles/nest-thermostat-savings/).
## Tools Used
To ensure that my writing is professional, I have used Writefull for spelling and grammar, and OpenAI’s Bing Chat to help me structure my report.