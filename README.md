# Image Crop Analysis: Unintentional Harms of Cropping Accessibility Mobility Aids

I am submitting my inquiry into how the Twitter saliency model crops images of disabled people who use accessibility mobility aids, such as wheelchairs and canes. Mobility aids are a critical mechanism for physical mobility and empowerment (Ladner, 2015). Disabled people who use mobility aids have described their aids as being an integral component of their identity. Some disabled people customize and decorate their aids as a source of pride and as a way to resist socio-cultural stigma of disability (Profita, 2016). Therefore, my submission is based on the premise that an image of a person with their accessibility aid should include their aid in the cropped image to embrace their full identity. An algorithm that crops out a person’s aid is creating unintentional harm.

I performed an analysis of a small sample: 20 images of people in wheelchairs; 20 images of blind people using a cane; and 20 images of people with mobility disabilities using a walking cane. I use images I found by doing a Google search of “people in wheelchairs,” “blind person using cane,” and “person using walking cane,” respectively. In my image sample, I made sure to include a diversity of gender and race since it is important to consider the intersectionality of the disability population.

To summarize my analysis, the majority of images DO include at least some portion of the accessibility aid, which is very promising. However, I found instances in which the saliency model DOES crop out cane or wheelchairs, resulting in an image that erases a crucial component of disability identity. Due to the importance of understanding this issue more in-depth, I strongly encourage further investigation of a quantitative and qualitative nature, described here and in my LIMITATIONS section.  To determine a more reliable impact, a larger sample of images would need to be analyzed. Those images should account for intersectionality since disabled people are of different races, genders, and other identities. I found some instances in which the intersection of identities (female-presenting & disabled) resulted in an image crop that focused on the torso of the individual, thus introducing harm on multiple dimensions. I detail the specifics of these instances in the RESULTS section below. 

To gauge the potential impact of this harm, I start with the demographic provided by the World Health Organization (2020):  worldwide, there are over one billion people with a disability, according to the World Health Organization.There are approximately xx people with mobility impairments who may use canes.  As of 2011, 75 million people need a wheelchair on a daily basis. Note that this represents 1% of the world’s population (World Health Organization, 2011). ” Regarding blindness, there are approximately 88.4 million blind people worldwide (World Health Organization, 2021). 

# Findings

Here I report on the issues I found based on my qualitative review of the “Image Crop Analysis” notebook. (Note that I have the images and issues listed in “Zolyomi Twitter Saliency Mobility Aids.PDF” uploaded to my GitHub repository.)

I list these in order that I have the images in the PDF. As for priority, I would assess the highest priority issues to be those about cropping disabled people (while leaving in non-disabled people or animals) and cropping out portions or all of aids. In some cases, the aid is close to the crop line indicating that there is no priority given to the object. One idea to pursue is labeling images with aids as part of the machine learning training so the algorithm assigns higher priority to accessibility aids.

Issue: Mobility Cane 8: crop out cane in ar=1.4; ar=2.00 crops out one person with cane, but leaves other person with cane. Investigate what image cropping does when multiple people are using aids.
Issue: Wheelchair 13: Sign is marked as saliency point. Ar=1.00 and ar=2.00 crop leaves out people.
Issue: Cane 17: ar=2.0 puts priority on person without cane, therefore cane is cropped out 
Issue: Mobility cane 18: ar=2.0 crops out his left-hand cane. More exploration needed of people using multiple aids.
Issue: Cane 13: ar = 2.0 crops out full body and aid
Issue: mobility cane 7: Cane is not given additional weight in saliency model, so it is neglected in ar=1.00 and ar=1.14. Person and cane cropped out of ar=2.00
Issue: Cane 8: ar=2.0 includes cane but not person using cane. Area to explore is if aid is shown without person.
Issue: Mobility cane 11: Most salient point is on person in background, not disabled person in foreground. Ar=2.0 includes aid, but crops half of disabled person.
Issue: Mobility cane 13: Image with text and disabled person; saliency point is on text rather than person. Ar=1.0 and ar=1.14 cuts person off at torso or below and crops part of cane, making it hard to identify. 
Issue: Cane 5: As with many of these images, ar=0.56 is a horizontal crop and often leaves out or drastically cuts a person’s mobility aid. Ar=2.0 prioritizes right portion of image, cropping half of mobility aid on the left portion of the image. 
Issue: Cropping for ar=.56, 1, and 1.14 crop out the person’s cane.
Issue: Cane 18: Saliency point is on dog’s face not human’s face. Ar=.56, 1.00, and ar=1.14 crop off disabled person’s face.
Issue: Cane 18: Saliency point is end of cane, not human’s face. Ar=.56, 1.00, and ar=1.14 crop off disabled person’s face.
Issue: Cane 15. Saliency point is on left-hand side of image rather than center of group of people. Results in crops that include extra, less relevant background rather than people.
Issue: Mobility cane 2: Horizontal crop focuses on bottom portion of image, not person’s face. 
Issue: wheelchair 19: saliency point is on people in background, not person in foreground in wheelchair
Issue: mobility cane 14:  ar=2.0 crops out red cane.
Issue: wheelchair 15: ar=1.00 crops disabled person in half (leaves 2 abled-bodied people entact); ar=1.14 keeps child’s legs but crops rest of her body, face, and wheelchair; ar=2.00 crops out disabled person and aid entirely

# Limitations

People have different connections and relationships with their assistive aids. For example, the role of assistive aids in people’s identities varies. Some people may not consider their aid as an integral aspect of their identity, and thus, may not have a strong negative reaction to their accessibility aid cropped from an image. Some wheelchair users will have different opinions and associations related to their wheelchairs depending on how long they have been using a wheelchair and other factors (Carrington et al., 2014). Further research is needed to determine disabled people’s attitudes toward image cropping of mobility aids and other visual aspects of disability, such as prosthetics. 

Also, I acknowledge that my analysis is qualitative and that I did my analysis based on looking at the results of the “Image Crop Analysis” and ar cropping rectangles. (As I was learning about this Bounty initiative and familiarizing myself with Jupyter notebooks, I did run a process that output (I believe) the most likely resulting cropped image. Hower, today I am unable to remember how to generate those images. I’d be happy to collaborate with someone to analyze additional output of the Twitter saliency notebooks.)

#Self-Grading Recommendation

Harm Base Score: Underrepresentation has a base score of 20 points.
 
Multiplier Factors:
Damage: I demonstrated harm along the dimension of disabled people and point to the need for further investigation of additional dimensions (intersectionality of race & gender, people with multiple disabilities, plus evaluating images of disabled and non-disabled people). Measure to the impact to population overall is 1.2 To be conservative, I am assessing damage of (1.2 + 1.2)/2 = 1.2.
Affected Users: I demonstrated this impacts more than one million but less than one billion people on our platform (Affective User Score = 1.2)
Likelihood or Exploitability:
This harm is estimated to have occurred on Twitter monthly (Likelihood = 1.1)
Submitted harm was classified as an unintentional harm therefore I receive no exploitability grade.
Justification: Findings were considered strong but could have been improved by using a larger, better labeled data set. The submission contained a detailed qualified explanation of how harms impacted affected people. (Justification = 1.0)
Clarity: The submission included detailed instructions and notebooks that allowed any person to reuse our methodology. Limitations of the methodology and the data used in analysis were culturally situated and well documented. (Clarity = 1.25)
Creativity: This submission exercised industry standard methods for assessing ableist harms so did not qualify for additional creativity / wild card multipliers.
 
The overall score of my Accessibility Aids bias assessment is:
20 base points x MF(1.2 + 1.2 + 1.1 + 1.0 + 1.25) which is (20 x 5.75) for a total score of 115. (Please check my calculation because I see in the example that the example total was 60.84 and my factor values are very similar.) 

# References

Carrington, Patrick, Amy Hurst, and Shaun K. Kane. “Wearables and Chairables: Inclusive Design of Mobile Input and Output Techniques for Power Wheelchair Users,” 3103–12. ACM Press, 2014. https://doi.org/10.1145/2556288.2557237.

Ladner, Richard E. “Design for User Empowerment.” Interactions 22, no. 2 (2015): 24–29.

Profita, Halley P., Abigale Stangl, Laura Matuszewska, Sigrunn Sky, and Shaun K. Kane. “Nothing to Hide: Aesthetic Customization of Hearing Aids and Cochlear Implants in an Online Community.” In Proceedings of the 18th International ACM SIGACCESS Conference on Computers and Accessibility, 219–27. Reno Nevada USA: ACM, 2016. https://doi.org/10.1145/2982142.2982159.

World Health Organization. 2020. Disability and Health. Retrieved August 6, 2021 from https://www.who.int/news-room/fact-sheets/detail/disability-and-health.

World Health Organization. World Report on Disability. 2011. Retrieved August 6, 2021 from https://www.who.int/disabilities/world_report/2011/report.pdf. 

World Health Organization. Blindness and Vision. 2021. Retrieved August 6, 2021 from https://www.who.int/news-room/fact-sheets/detail/blindness-and-visual-impairment. 
