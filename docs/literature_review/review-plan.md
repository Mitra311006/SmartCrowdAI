# Literature review plan

**Project:** AI-Based Smart Crowd Understanding using Vision Foundation Models for Real-Time Safety and Risk Prediction  
**Review question:** How can crowd perception, temporal behavior analysis, uncertainty estimation, and evidence-grounded explanations be combined and evaluated for timely, actionable crowd-safety risk prediction?

## Scope and review stance

Treat context-aware, uncertainty-aware risk prediction with evidence-grounded explanations as a **hypothesis to investigate**, not an assumed novel contribution. Distinguish three things throughout: (1) findings directly reported in verified papers, (2) the authors’ own stated limitations, and (3) our project hypotheses/gap candidates requiring confirmation through a broader, systematic search. Avoid claiming novelty until relevant work has been searched across adjacent fields.

## Review questions and topic map

1. **Crowd counting and density estimation:** image- versus video-based count; density maps; perspective/scale variation; counting under occlusion; video identity/entry reasoning; datasets, annotations, transfer and real-time constraints.
2. **Video-based crowd anomaly detection:** normality modelling, reconstruction/prediction, weak/semi/fully supervised methods, spatiotemporal and graph methods, localization, crowd-specific versus general video anomalies, event labels, false alarms and deployment latency.
3. **Vision Foundation Models (DINOv3, SAM 2, CLIP):** pretraining and intended capabilities; dense features, promptable segmentation/tracking, image-text alignment; adaptation/fine-tuning or prompting for crowded scenes; compute, temporal limitations, and empirical transfer evidence. Keep technical reports/preprints distinct from peer-reviewed publications.
4. **Explainable AI for visual surveillance:** saliency/localization, concept- or example-based explanations, verbal explanations, evidence traceability, explanation faithfulness, human usability, privacy and failure modes.
5. **Vision-Language Models for video understanding:** video input and temporal grounding, streaming/online inference, captioning and dialogue, event recognition/forecasting, hallucination control, latency and evaluation of generated summaries.
6. **Real-time risk prediction and uncertainty:** define risk outcome and forecast horizon; separate hazard/density/anomaly scores from calibrated risk; epistemic/aleatoric uncertainty, calibration, abstention/alerts, lead time, alert burden, throughput and end-to-end latency.

## Search and screening protocol

Search IEEE Xplore first for peer-reviewed IEEE work from 2022–2026, then cross-check records in the publisher proceedings/journal, DOI/Crossref, or another accessible scholarly index. Add foundational and seminal work regardless of year, plus relevant non-IEEE scholarship where the area warrants it. Search adjacent terms, not just project phrasing: crowd counting, crowd density estimation, crowd flow, crowd anomaly/abnormal event, video anomaly detection, visual surveillance XAI, video-language model, streaming video, crowd risk, crowd crush/stampede, uncertainty/calibration. Record query, source, date, and screening decisions in the eventual review log.

Include peer-reviewed primary studies, surveys for discovery/context, and clearly labeled preprints/technical reports when directly relevant (for example DINOv3/SAM 2). Exclude unverifiable citations and papers without a defensible connection to a review question. For each retained work, verify title, author list, year, venue and DOI/official URL; capture dataset, metrics, numerical findings and limitations only from accessible primary sources. If unavailable, write “not verified” rather than infer.

## Comparison and synthesis

Use `comparison-template.md` to extract one paper per row. Tag each paper by topic and evidence type (peer-reviewed primary study, survey, preprint/technical report). Compare methods only within compatible tasks/datasets/metrics; do not rank results across unlike protocols. For proposed gaps, cite the compared evidence and label the statement **Project hypothesis**, not literature fact. Synthesize cross-topic dependencies: perception quality → temporal tracking/flow → anomaly/risk signal → calibrated alert → evidence-linked explanation/summary → dashboard and operational evaluation.

## Evaluation questions for the eventual project

Plan to report task-appropriate count error and density-map measures; tracking metrics where identities are used; anomaly detection/localization measures; risk calibration and discrimination; event lead time and false-alert burden; explanation grounding/faithfulness and human review; summary factuality; and end-to-end latency/FPS on stated hardware. Specify camera conditions, privacy safeguards, dataset splits, domain shift, and failure analysis. Do not imply that model FPS alone establishes a real-time safety system.

## Verified starter references (not an exhaustive review)

The following bibliographic records were checked against the linked scholarly/official records. Reported result/method details should still be rechecked in the primary text before quantitative comparison.

- Han et al., “DR.VIC: Decomposition and Reasoning for Video Individual Counting,” CVPR 2022, [official CVF paper](https://openaccess.thecvf.com/content/CVPR2022/html/Han_DR.VIC_Decomposition_and_Reasoning_for_Video_Individual_Counting_CVPR_2022_paper.html), [DOI](https://doi.org/10.1109/CVPR.2022.00314). Peer-reviewed video counting.
- Zhang et al., “Single-Image Crowd Counting via Multi-Column Convolutional Neural Network,” CVPR 2016, [official CVF paper](https://openaccess.thecvf.com/content_cvpr_2016/html/Zhang_Single-Image_Crowd_Counting_CVPR_2016_paper.html). Foundational density estimation.
- Li et al., “CSRNet: Dilated Convolutional Neural Networks for Understanding the Highly Congested Scenes,” CVPR 2018, [official CVF paper](https://openaccess.thecvf.com/content_cvpr_2018/html/Li_CSRNet_Dilated_Convolutional_CVPR_2018_paper.html). Foundational congested-scene density estimation.
- Yang et al., “Evolving graph-based video crowd anomaly detection,” *The Visual Computer* 40(1), 2024 (online 2023), [DOI](https://doi.org/10.1007/s00371-023-02783-4). Crowd-specific video anomaly detection.
- Zhang et al., “Exploiting Completeness and Uncertainty of Pseudo Labels for Weakly Supervised Video Anomaly Detection,” CVPR 2023, [DOI](https://doi.org/10.1109/CVPR52729.2023.01561). General video anomaly detection, not crowd-only.
- Radford et al., “Learning Transferable Visual Models From Natural Language Supervision,” ICML 2021, [PMLR record](https://proceedings.mlr.press/v139/radford21a.html). Foundational CLIP.
- Ravi et al., “SAM 2: Segment Anything in Images and Videos,” 2024 technical report, [arXiv](https://arxiv.org/abs/2408.00714). Not treated as peer-reviewed absent a verified proceedings record.
- Siméoni et al., “DINOv3,” 2025 technical report, [arXiv](https://arxiv.org/abs/2508.10104). Not treated as peer-reviewed absent a verified proceedings record.
- Ye et al., “VERA: Explainable Video Anomaly Detection via Verbalized Learning of Vision-Language Models,” CVPR 2025, [DOI](https://doi.org/10.1109/CVPR52734.2025.00811). Explainable video anomaly detection.
- Selvaraju et al., “Grad-CAM: Visual Explanations from Deep Networks via Gradient-Based Localization,” ICCV 2017, [DOI](https://doi.org/10.1109/ICCV.2017.74). Foundational visual explanation, not surveillance-specific.
- Chen et al., “VideoLLM-online: Online Video Large Language Model for Streaming Video,” CVPR 2024, [official CVF paper](https://openaccess.thecvf.com/content/CVPR2024/html/Chen_VideoLLM-online_Online_Video_Large_Language_Model_for_Streaming_Video_CVPR_2024_paper.html). Streaming video-language understanding.
- Tang et al., “Video Understanding With Large Language Models: A Survey,” *IEEE Transactions on Circuits and Systems for Video Technology*, 2025, [DOI](https://doi.org/10.1109/TCSVT.2025.3566695). IEEE survey; consult the full record/article before summarizing conclusions.
- Subramanian and Verma, “Crowd risk prediction in a spiritually motivated crowd,” *Safety Science* 155, article 105877, 2022, [DOI](https://doi.org/10.1016/j.ssci.2022.105877). Crowd risk in a specific context; not verified as vision-based.
- Oh et al., “Crowd Counting with Decomposed Uncertainty,” AAAI 2020, [DOI](https://doi.org/10.1609/aaai.v34i07.6852). Uncertainty in crowd counting, not calibrated crowd-risk forecasting.
- Sabokrou et al., “Real-time anomaly detection and localization in crowded scenes,” CVPR Workshops 2015, [DOI](https://doi.org/10.1109/CVPRW.2015.7301284). Earlier crowd-specific anomaly reference.
- Deng et al., “Deep learning in crowd counting: A survey,” *CAAI Transactions on Intelligence Technology* (online 2023; issue 2024), [DOI](https://doi.org/10.1049/cit2.12241). Non-IEEE survey useful for method/dataset discovery.

**Preliminary hypotheses to test (not established gaps):** the selected seed papers do not yet demonstrate one evaluated system that jointly links crowd perception, calibrated operational risk forecasts, and evidence-grounded explanations under a real-time constraint; and generic foundation-model/video-language capabilities may not transfer reliably to crowded surveillance scenes without task-specific evaluation. Broaden the search before claiming either gap or novelty.

**Coverage caveat:** this is a verified starter set, not a systematic or exhaustive search. The starter list has recent IEEE/CVF work in video counting, video anomaly detection, explainability and streaming video, but needs additional IEEE Xplore searches for 2022–2026 crowd-specific density-estimation and operational risk papers. Add verified 2026 publications only when accessible records substantiate them.
