---
weight: 2
bookCollapseSection: false
title: "Beyond the Wrist: Debugging RSI"
---

# Beyond the Wrist: Debugging RSI

This is a personal essay about a period of major suffering from chronic pain I went through, and how I acquired the knowledge and skill to eventually lift me out of it. 

---

## **A fire burning**

I am about to give up. My eyes are bleary after four days of staring at numpy arrays. I want to smash my keyboard and throw it out into the snow, but I have promised myself that I will fix this bug by the end of the week.

Besides a dull headache, I feel the usual ache in my wrists. This time, though, my forearms are also hurting. A dull heat rises from my wrists to the soft muscle below my elbow. Another half hour of coding, the pain in my wrists becomes sharper. So I stop for the day, knowing that my wrists will be back to normal enough to fix this problem tomorrow. Or so I think.

As a grad student in CS, I code a lot, so make sure to have good postural and ergonomic hygiene. I use a Microsoft Sculpt keyboard, hotkeys to minimize mouse use. My wrists are neutral and my screen is at head height. It more or less keeps various aches at bay.

The next morning, wrists sore, I begin to type, and within fifteen minutes, the dull heat in my forearms becomes hot. My fingers become stiff; my typing slows to a crawl. My hands feel like they have been submerged in snow – cold, inflexible, useless.


In the doctor’s office, I explain the situation:

> **Me** (suppressing panic, explaining the situation): What’s going on?
>
> **Doctor**: You have tendonitis or a repetitive strain injury — the tendons in your hand are inflamed from overuse.
>
> **Me**: You’re saying my hand is damaged from me typing too much? But I’m actually typing less than I was last semester.
>
> **Doctor** (shrugging): To be honest, we don’t really know what’s going on. But you should see a physiotherapist. It’s up to you, but here’s a referral slip.

The physiotherapist tells me my muscles are imbalanced — some auxiliary muscles need strengthening. She gives me wrist exercises. 

I am confused. Last semester I was spending twice the time typing than I am now. Also, before this flare up, I could do pull-ups just fine. Muscle and tendon weakness can’t be the cause.

Four weeks later and it’s even worse. I’m using my forearms to open doorknobs, eating frozen meals because I can’t chop vegetables, and wondering if I have to use voice dictation software for the rest of my life. I move between fear and anger as my waking states.

I start looking for solutions and order a dozen pop-sci books about chronic pain, and start doing a literature review:

A couple books in, it hits me: **I, the doctor, and the physiotherapist are all working at the wrong level of abstraction**.

Of course we could look at the pain at the level of my _extensor carpi radialis_, but what becomes blindingly obvious is that **pain is complex and distributed**. There is no pain center in the brain [^1]. Everywhere from the somatosensory cortex to the amygdala to the vagus nerve to nociceptors in our skin is involved in the unpleasant experience we call pain.

I began to suspect that my situation was more like a _software_ problem than a _hardware_ problem. Rather than any part of my wrist or forearm having structural damage, my pain was a prediction system gone awry.

After doing five hours of exercises that looked like they had nothing to do with my wrists — there was a major shift. Though I still felt sharp in my wrist, my forearm was down to a low burn. Three months later, and I was doing pull-ups and typing again — no sharpness, no burn, _nothing_.

The rest of this post is about the mechanism of pain that I uncovered and what I did to become functional again.


## **Understanding pain as inference**

Disclaimer: There is a lot that we don't understand about pain. The account I’m about to give is a broad overview of the features of pain consistent with the literature on the neuroscience of pain. I cite the relevant resources that have contributed to this impression at the bottom.

 


### **1. The old account: pain as measure of damage**

Both the physiotherapist and the doctor told me to _rest my wrist_. Why? Because they believed that my pain was from a wrist that was inflamed and damaged by continued activity. ‘Repetitive strain injury’ as a diagnosis implies that it is the repetitive motion that is causing damage and therefore pain.

Their model was something like:

**Tissue damage → Nociceptors response → Experience of pain**
{{< katex display=true >}} \text{Tissue damage} \rightarrow \text{Pain receptors fire} \rightarrow \text{Experience of pain} {{< /katex >}}
{{< katex display=true >}} \text{thus} {{< /katex >}}
{{< katex display=true >}} \text{Pain} \implies \text{Tissue damage} {{< /katex >}}

Logically, the available treatments become either 'fixing' the tissue damage by doing wrist exercises to ‘balance’ the muscles in my forearm, or taking an NSAID like Advil to chemically inhibit the [nociceptive response](https://en.wikipedia.org/wiki/Nociception).

 


### **2. Cracks in the model**

This didn’t make sense in light of my experience. Some days I had fairly little pain while other days it was debilitating — but I was keeping them in wrist braces and minimizing use on both days. It would be very strange if it was increased damage that was causing more pain. Also, I noticed that the location would shift slightly. Some days it would radiate more up my forearms while other days it would center around my wrists. How could the sensation be changing if it was just from tissue damage?


As I started to explore the literature more, I saw that it also didn’t make sense with other people’s experiences:


* People had pain with no damage
    * People who have had limbs amputated often report intense pain in the absent limb. The pain is usually intermittent, and is often vividly described as throbbing, stabbing or burning. They are able to distinguish between pain at the stump, and pain within the missing limb itself. In this case, there is no tissue damage in the absent limb, yet there are recurring episodes of pain long after the wound has healed.
    * Emotional pain: whether the death of a loved one, or  heartbreak, **some of the most painful experiences we go through involve no physical damage**.
* People had damage with no pain
    * Henry Beecher, an anesthesiologist on the battlefield of the Anzio Beachhead in Italy during WWII, found an astounding lack of reported pain among severely wounded soldiers. He surveyed the reported pain intensity of 215 lucid men that had penetrating wounds in the head, chest, or stomach, compound bone fractures, or extensive soft-tissue wounds. **Three-quarters of the soldiers with severe wounds had so little pain that they refused pain relief medication[^2].**
    * 

 


### **3. Pain is prediction of future damage**

Here's a more useful account of pain.

Brains evolved in multicellular organisms because they could predict the needs of other organ systems and take action to keep the organism alive.

It’s why your thirst is quenched within thirty seconds of drinking water even though it takes thirty minutes for your small intestine to reabsorb it. It’s also why you salivate when just smelling food as you pass by, or start to shiver in the cold even when your core body temperature hasn’t dropped. 

**Pain is a signal for protective action. Not a damage meter.** When we touch a hot stove, we yank our hand away — often quick enough to avoid any damage. If our hand is burned, we keep it close to our body, away from accidental bumps that might damage it.

It's worth remembering that the brain is a folded sack of flesh sealed in thick bone box. And that it understands basically everything through pipes that carry chemicals and digital signals. There is no such thing as 'ground truth' to the brain, so it has incorporate different signals to make predictions.

Our brains use many different signals to make predictions. One of the most highly weighted signals is fear. You've felt this if, stepping out of a scary movie, you were startled by the shadow of some harmless pedestrian. Or if you've gotten an injection in a strange foreign office where the nurse is mean, and then another where she/he is chatting with you and you're relaxed — _it literally hurts more when you're scared_.

 


### **4. My pain prediction system was miscalibrated**

So what was going on with my wrist pain? Basically, the intensity and stress with which I was coding contributed to initial sensation in my forearm. But then there was a vicious feedback loop. 

Because I interpreted the pain as “something wrong with me”, I became more afraid when my wrist hurt, which then amplified the pain. This repeated until it became debilitating for me.

 

A simplified version of what was going on:

{{< figure src="/images/simple_diagram_pain.png" alt="drawing" width="400" >}}

My pain system was miscalibrated to the environment. It was predicting future damage, fed by stress and the fearful belief that “something is wrong with my wrist”, **even though my wrist was structurally fine**.


### **Recalibrating my pain system**

**The understanding alone decreased my pain.**

Coming to internalize that _pain is not damage_ and that _my wrist was not in danger_, made a big difference. Once upon a time, I would have doubted that a change in my beliefs could change something as intimate as my experience of pain. But the experience was undeniable — and made sense in context of the predictive brain.

The internalization happened over many different resources. Papers[^3], books[^4], videos[^5], conversations with a neuroscience professor. The books and lectures tend to be helpful in tone, but have models that I think are outdated or imprecise; the papers are precise enough but hard to internalize emotionally.

I would say this brought me ~50% towards resolution.

 

**Shifting from a default stress-fear state**

Many different approaches worked for me through different periods of time. I initially looked very briefly at[ the literature](https://www.cochrane.org/CD002014/BACK_behavioural-treatment-for-chronic-low-back-pain) comparing different treatments for chronic pain, and concluded that I would learn far more from just experimenting by myself. I'm very glad that I did.

At the beginning, I played around with something like a combination of[ Focusing](https://www.lesswrong.com/posts/PXqQhYEdbdAYCp88m/focusing-for-skeptics) and[ IFS](https://www.lesswrong.com/posts/5gfqG3Xcopscta3st/building-up-to-an-internal-family-systems-model)-like practices. Then, I found[ Pain Reprocessing Therapy](https://www.painreprocessingtherapy.com/), which basically works by shifting priors through gentle awareness exercises[6]. They don’t use the language of predictive processing, but I found PP a better frame than their own to understand their proposed practices of “somatic tracking” and “positive affect induction”.

I did these awareness exercises on my own, and eventually went through their certification program to teach PRT, which improved my own ability to do the exercises. 

These got me another 40% to resolution.

At this point, I was actually better than before the first spreading of heat into my forearms. 

The last 10% was from gradually finding the tasks that would trigger pain, and doing them from a calm place until I could do them consistently while staying calm.

 

**A high level model of what happened**


<!-- 
![Alt text for the image](/images/complex_diagram_pain.png) -->

{{< figure src="/images/complex_diagram_pain.png" alt="drawing" width="500" >}}


My model of what happened is something like this: initially, my brain had a strong prior of my wrists being damaged, which influenced lower level predictions of pain (and thus experiences of pain) during periods of extended usage. This prior was reinforced by the fear and stress associated with the pain, creating a feedback loop that led to higher precision (certainty) for these pain predictions for longer periods. 

New information ("your wrists might not be damaged") shifted my higher-level priors, which also decreased the lower level predictions of pain, stopping that feedback loop. Still, the emotional state of stress and fear were persistent, and doing the Focusing/PRT relaxed my nervous system and also decreased the low level pain priors. It is also consistent with the model proposed by Hechler et al. (2016) I reference below. 

 

I am confident this explanation is directionally correct, based on my direct experience. I went from having fingers that would visibly seize up when trying to type, to being able to play guitar and chop vegetables without pain.

While it might seem like regression to the mean or some other physiological shift could explain my recovery, what solidifies my confidence in the feedback loop model is the real-time changes I observed. _Within a single day, I could sense the pain changing as I performed an exercise_. As I made this a habit, it became increasingly clear that a process similar to what I've described above was taking place. This immediate and consistent correlation between my mental exercises and pain levels strongly suggests that the mechanism was more than just natural healing or coincidence.

I was convinced that this was not uncommon from conversations with two friends who went through a similar arc, and the [thousands of testimonials](https://www.tmswiki.org/forum/tags/wrist/) of people online who had their wrist pain resolved through similar means. I'm now in the process of formalizing this intuition and writing it up.

It's now been a couple years since the incident, and I've had one mild episode of pain where I paused from playing the piano for a week — but otherwise my wrists have been happy and healthy.

I'm not suggesting that what I did will work for everyone. But, given the low monetary cost and risk of harm, and fairly high upside — I think some experimentation in this vein is at least something to seriously consider. 

Quick note on possible risks: I have not heard of people worsening their pain condition through any of the exercises I described above. Perhaps the worst outcome would be not going to the doctor when you have a malignant tumor on your wrist, or a fractured bone. I'm not discouraging normal medical attention.

**Acknowledgements**

I want to thank the generation of pain researchers that laid the groundwork for this understanding. Even as some of their theories have been superseded, pioneers like George Engel, John Sarno and Ronald Melzack created the foundational building blocks for discussions like this to happen. Also to Professor Fan Wang for her mentorship and support.

 


{{< hint info >}}
### Postscript

Since my recovery, it's become clearer to me that processing your own pain is a learnable skill. I've since had the opportunity to teach several people this skill, using my own idiosyncratic interpretation of pain reprocessing therapy (PRT). This has led me to believe that there's room to refine and improve the efficacy of existing techniques. 

EDIT: I'm running a [live course]({{< relref "/posts/cohort_nov24.md" >}}) teaching you these skills starting mid-November. 

Continue reading at [Pain Debugging Protocol]({{< relref "../practice/pillars_of_practice.md" >}})

{{< /hint >}}





**References**:


[^1]: See the discussion of the ‘neuromatrix’ in Melzack, Ronald. "Pain and the neuromatrix in the brain." _Journal of dental education_ 65.12 (2001): 1378-1382.

[^2]: Beecher, Henry K. "Pain in men wounded in battle." Annals of surgery 123.1 (1946): 96. The study is not perfect, but for my purposes it holds true.

[^3]: Hechler, Tanja, Dominik Endres, and Anna Thorwart. "Why harmless sensations might hurt in individuals with chronic pain: about heightened prediction and perception of pain in the mind." Frontiers in psychology 7 (2016): 1638.; Büchel, Christian, et al. "Placebo analgesia: a predictive coding perspective." Neuron 81.6 (2014): 1223-1239.; Stilwell, Peter, and Katherine Harman. "An enactive approach to pain: beyond the biopsychosocial model." Phenomenology and the Cognitive Sciences 18.4 (2019): 637-665.; Ashar, Yoni K., et al. "Effect of pain reprocessing therapy vs placebo and usual care for patients with chronic back pain: a randomized clinical trial." JAMA psychiatry 79.1 (2022): 13-23.

[^4]: Butler, David Sheridan, and G. Lorimer Moseley. Explain Pain 2nd Edn. Noigroup publications, 2013.; Hargrove, Todd R. "A guide to better movement: the science and practice of moving with more skill and less pain". Better Movement, 2014.; Zoffness, Rachel. "The pain management workbook: Powerful CBT and mindfulness skills to take control of pain and reclaim your life". New Harbinger Publications, 2020.
[^5]: [Schubiner lecture](https://www.youtube.com/watch?v=0VyH1laOd2M),[ rambling but convincing (to me) testimonial](https://www.youtube.com/watch?v=vAS7HdsM4DY&t=1005s), (see the various thumbnails from these videos)
[^6]: I am not fully satisfied by their proposed model of what their practices are doing, but in either case it worked for me and most others I've shown.
[^7]: Ashar et al (2022) found 66% of back pain patients had dramatic decreases in pain from 4 weeks with PRT (which persisted after 1 year), and I think it's possible to do even better. Both in terms of the fraction of people that can be helped, and the time required before significant change.
