# A. EXPERIMENTAL DETAILS

This section provides experimental details for all research con-
ducted, including LLM model size, temperature, and testing envi-
ronment parameters.

## A.1 Text generalisation by RTT
The PAIR attacks are targeting GPT4, Vicuna-13b-v1.5, Llama-2-13b-chat-hf, and PaLm2. The temperature is set to 0 if available as an
adjustable parameter, which is same as the PAIR paper’s original setting [1].

## A.2 Increase of adversarial prompts’ global intrinsic dimension after RTT
The GID estimation by the Persistent Homology Estimator estimation follows the default setting in the original paper [7 ], i.e. MIN_SUBSAMPLE
= 40, INTERMEDIATE_POINTS = 7, PHD (alpha=1.0, metric=’euclidean’, n_points=9). Note that we will use the maximum likelihood estima-
tion from the same paper to estimate the GID for prompts with less than 40 tokens, but there were less than 10 occurrences among 700
testing samples.
The PAIR attacks are targeting GPT4, Vicuna-13b-v1.5, and PaLm2. The temperature is set to 0 if available as an adjustable parameter. The
SAP attack targets GPT-3.5-turbo with temperature = 1, which is the same as the setting in the original paper [3].
All the benign and adversarial prompts are randomly sampled from their original dataset

## A.3 Number and type of translated languages for RTT
The non-Indo-European languages we used are as follows: Amharic, Arabic, Aymara, Bambara, Basque, Chinese (Simplified), Chinese
(Traditional), Corsican, Divehi, Dogri, Esperanto, Ewe, Guarani, Haitian Creole, Hausa, Hawaiian, Hmong, Igbo, Iloko, Indonesian, Japanese,
Javanese, Kazakh, Khmer, Kinyarwanda, Konkani, Korean, Krio, Kurdish, Kurdish (Sorani), Kyrgyz, Lao, Latin, Lingala, Luganda, Maithili,
Malagasy, Malay, Malayalam, Maori, Marathi, Manipuri, Mizo, Mongolian, Burmese, Chichewa, Oromo, Samoan, Sanskrit, Scottish Gaelic,
Sesotho, Sesotho (Southern Sotho), Shona, Sindhi, Sinhala, Sundanese, Swahili, Tagalog, Tajik, Tamil, Tatar, Telugu, Thai, Tigrinya, Tsonga,
Turkish, Turkmen, Akan, Uighur, Uzbek, Vietnamese, Xhosa, Yoruba, Zulu.
The personal computer we used for measuring the time required for applying RTT3d on one query is MacBook Pro, Apple M1 Max, 64 GB
Memory

## A.4 Transferability of RTT defense in LLMs
The PAIR attacks are targeting GPT4, Vicuna-13b-v1.5, Llama-2-13b-chat-hf, and PaLm2. The temperature is set to 0 if available as an
adjustable parameter, which is the same as the PAIR paper’s original setting [1].

## A.5 Comparing RTT with other paraphrasing techniques
The temperature of GPT4 is set to 0.
When we conducted the paraphrasing experiments above, we found that GPT4 sometimes failed to follow our paraphrasing requests, and
simply output the original text. Note that we manually ensure the accuracy of GPT4’s paraphrasing before recording data in all experiments

## A.6 Comparing RTT with other defenses
The PAIR attack targeted Vicuna-13b-v1.5. The settings of SmoothLLM and SelfDenoise are both set to default from their original papers,
with 30% of perturbation scale [4, 6].

## A.7 RTT on other adversarial attack
All the adversarial attacks are generated according to the default settings from their papers or directly imported from their GitHub [ 3, 8 , 9 ].
The 200 SAP adversarial attacks are randomly sampled from the SAP200 datasets with topics of fraud, politics, race, religion, suicide,
terrorism, and violence [3],

## A.8 RTT on benign queries
All the benign queries are randomly sampled from their original
dataset [2, 5].

### References

[1] Patrick Chao, Alexander Robey, Edgar Dobriban, Hamed Hassani, George J Pappas, and Eric Wong. 2023. Jailbreaking black box large language models in twenty queries. arXiv
preprint arXiv:2310.08419 (2023).

[2] Karl Cobbe, Vineet Kosaraju, Mohammad Bavarian, Mark Chen, Heewoo Jun, Lukasz Kaiser, Matthias Plappert, Jerry Tworek, Jacob Hilton, Reiichiro Nakano, Christopher
Hesse, and John Schulman. 2021. Training Verifiers to Solve Math Word Problems. arXiv preprint arXiv:2110.14168 (2021).

[3] Boyi Deng, Wenjie Wang, Fuli Feng, Yang Deng, Qifan Wang, and Xiangnan He. 2023. Attack prompt generation for red teaming and defending large language models. arXiv
preprint arXiv:2310.12505 (2023).

[4] Jiabao Ji, Bairu Hou, Zhen Zhang, Guanhua Zhang, Wenqi Fan, Qing Li, Yang Zhang, Gaowen Liu, Sijia Liu, and Shiyu Chang. 2024. Advancing the Robustness of Large
Language Models through Self-Denoised Smoothing. arXiv preprint arXiv:2404.12274 (2024).

[5] Arindam Mitra, Hamed Khanpour, Corby Rosset, and Ahmed Awadallah. 2024. Orca-Math: Unlocking the potential of SLMs in Grade School Math. arXiv:2402.14830 [cs.CL]

[6] Alexander Robey, Eric Wong, Hamed Hassani, and George J Pappas. 2023. Smoothllm: Defending large language models against jailbreaking attacks. arXiv preprint
arXiv:2310.03684 (2023).

[7] Eduard Tulchinskii, Kristian Kuznetsov, Laida Kushnareva, Daniil Cherniavskii, Sergey Nikolenko, Evgeny Burnaev, Serguei Barannikov, and Irina Piontkovskaya. 2024. Intrinsic
dimension estimation for robust detection of ai-generated texts. Advances in Neural Information Processing Systems 36 (2024).
[8] Zihao Zhou, Qiufeng Wang, Mingyu Jin, Jie Yao, Jianan Ye, Wei Liu, Wei Wang, Xiaowei Huang, and Kaizhu Huang. 2023. MathAttack: Attacking Large Language Models
Towards Math Solving Ability. arXiv preprint arXiv:2309.01686 (2023).
[9] Andy Zou, Zifan Wang, J Zico Kolter, and Matt Fredrikson. 2023. Universal and transferable adversarial attacks on aligned language models. arXiv preprint arXiv:2307.15043
(2023).
