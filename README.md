# Round Trip Translation Defence against Large Language Model Jailbreaking Attacks

## Abstract

Large language models (LLMs) are susceptible to social-engineered attacks that are human-interpretable but require a high level of comprehension for LLMs to counteract. The off-the-shelf defensive measures can only mitigate less than half of these attacks at most. To address this issue, we propose the Round Trip Translation (RTT) method, the first algorithm specifically designed to defend against social-engineered attacks on LLMs. RTT paraphrases the adversarial prompt and generalizes the idea conveyed, making it easier for LLMs to detect induced harmful behavior. This method is versatile, lightweight, and transferrable to different LLMs. Our defense successfully mitigated over 70\% of Prompt Automatic Iterative Refinement (PAIR) attacks, which is currently the most vigorous defense to the best of our knowledge. We are also the first to attempt mitigating the MathsAttack and reduced its attack success rate by almost 40\%. Our code is publicly available at google.com.

## Getting Started

We provide the python file `RTT.py` for Round Trip Translation with 3 different languages from non Indo-European Family. Please add your GOOGLE_APPLICATION_CREDENTIALS json file tp get started.
