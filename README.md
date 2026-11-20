# AarogyaMitra – Understanding Mind and Body
### An Agentic AI-Powered Mental Well-Being Support System

<p align="center">
  <strong>A Multimodal AI-Based Platform for Holistic Mental and Physical Wellness Assessment</strong>
</p>

---

## About the Project

**AarogyaMitra** is an Agentic AI-powered mental and physical well-being support system designed to provide users with a holistic understanding of their wellness.

The platform integrates Machine Learning, Computer Vision, Large Language Models (LLMs), and Multi-Agent AI orchestration to assess multiple dimensions of well-being and provide personalized wellness support.

Unlike conventional wellness applications that focus on individual aspects such as sleep, exercise, or mood tracking, AarogyaMitra combines multiple wellness indicators into a unified assessment framework.

The system evaluates six key wellness domains and uses specialized AI agents to provide context-aware recommendations, supportive interactions, recovery guidance, physical activity feedback, and navigation toward professional support.

**AarogyaMitra is intended as a wellness support platform and does not replace professional medical advice, clinical diagnosis, or treatment.**

---

## Key Features

- **Six-Domain Wellness Assessment:** Machine learning-based estimation of physical health, sleep recovery, psychological wellbeing, social wellbeing, lifestyle balance, and stress profile.
- **Psychological Wellbeing Screening:** Incorporates established self-report questionnaires such as WHO-5, PSS-10, PHQ-9, and GAD-7.
- **AI-Powered Wellness Assistant:** Supports personalized and context-aware wellness conversations.
- **Multi-Agent AI Architecture:** Uses specialized agents for psychological support, recovery, physical activity, and professional support navigation.
- **Yoga Posture Assessment:** Uses MoveNet-based body keypoint detection and joint-angle analysis to evaluate yoga posture against reference templates.
- **Stateful Agent Orchestration:** Uses LangGraph to coordinate agent execution, conditional routing, and workflow state transitions.
- **Context Management:** Uses an MCP-based context service layer for controlled wellness-context retrieval and persistence.
- **Document Verification:** Uses OCR-based text extraction to support information consistency checking from uploaded documents.
- **Persistent Wellness Profile:** Uses MongoDB for storing relevant user and assessment information.
- **Personalized Recommendations:** Provides wellness-oriented suggestions based on the user's assessment and interaction context.

---

## Wellness Domains

AarogyaMitra estimates wellness scores across six dimensions:

| Domain | Description |
|---|---|
| Physical Health | General physical wellness and health-related indicators |
| Sleep Recovery | Sleep duration, quality, consistency, and recovery |
| Psychological Wellbeing | Emotional state and psychological wellness indicators |
| Social Wellbeing | Social interaction and connectedness |
| Lifestyle Balance | Daily habits, routines, and lifestyle patterns |
| Stress Profile | Stress-related indicators and self-reported information |

The six-domain assessment provides a consolidated wellness profile that helps identify areas requiring attention.

---

## System Architecture

The system follows a modular, layered architecture that integrates user interaction, wellness assessment, machine learning, computer vision, agent orchestration, context management, and persistent storage.

### Overall Workflow

1. The user interacts with the React-based frontend.
2. The user provides questionnaire responses, lifestyle information, sleep information, and other relevant inputs.
3. The backend processes the collected information.
4. The Random Forest Regressor estimates scores across six wellness domains.
5. The generated wellness profile is passed to the agent orchestration workflow.
6. LangGraph manages workflow state and determines agent execution paths.
7. Specialized AI agents process the relevant wellness concerns.
8. The MCP-based context layer provides controlled access to relevant user context.
9. Agent outputs and relevant assessment information are persisted.
10. The AI Wellness Assistant presents personalized wellness guidance and recommendations.

### Specialized AI Agents

| Agent | Responsibility |
|---|---|
| Psychological Support Agent | Provides supportive conversations and wellness guidance based on psychological screening and user-reported information |
| Recovery and Wellness Agent | Evaluates sleep and recovery-related indicators and suggests suitable wellness activities |
| Physical Activity Agent | Assesses yoga posture using computer vision and provides posture-related feedback |
| Professional Support Navigation Agent | Helps users identify appropriate categories of professional support based on relevant risk indicators |

### Architecture Components

- Frontend and User Interaction Layer
- Wellness Assessment and Preprocessing Layer
- Machine Learning Prediction Module
- Computer Vision and Pose Assessment Module
- LangGraph Agent Orchestration Layer
- MCP-Based Context Management Layer
- Specialized AI Agents
- MongoDB Persistence Layer

---

## Technology Stack

| Category | Technologies |
|---|---|
| Frontend | React.js, Tailwind CSS |
| Backend | Python, FastAPI |
| Machine Learning | Scikit-learn, Random Forest Regressor |
| Computer Vision | MoveNet |
| Agent Orchestration | LangGraph |
| Context Integration | MCP-based service layer |
| Database | MongoDB Community Edition |
| OCR | Tesseract, PyTesseract |
| LLM Integration | Google Gemini API |

---

## Machine Learning Methodology

The machine learning component uses a Random Forest Regressor to estimate six wellness-domain scores.

### Dataset Information

- Dataset size: 25,000 synthetic records
- Model: Random Forest Regressor
- Number of estimators: 100
- Maximum depth: 15
- Missing-value handling: Median imputation
- Categorical encoding: One-hot encoding
- Random seed: 2026
- Evaluation: Independent 80/20 train-test split

### Reported Model Performance

| Wellness Domain | MAE | MSE | RMSE | R² |
|---|---:|---:|---:|---:|
| Physical Health | 7.316 | 84.837 | 9.211 | 0.788 |
| Sleep Recovery | 6.441 | 67.847 | 8.237 | 0.767 |
| Psychological Wellbeing | 8.988 | 126.274 | 11.237 | 0.670 |
| Social Wellbeing | 7.242 | 81.175 | 9.010 | 0.698 |
| Lifestyle Balance | 2.544 | 32.184 | 5.673 | 0.912 |
| Stress Profile | 7.494 | 88.432 | 9.404 | 0.790 |
| **Mean** | **6.671** | **80.125** | **8.795** | **0.771** |

**Note:** These results are based on synthetic data and an independent holdout evaluation. They do not establish clinical accuracy or real-world generalization.

---

## Computer Vision-Based Yoga Assessment

The Physical Activity Agent incorporates computer vision to evaluate yoga posture.

### Workflow

1. Capture the user's posture using a camera.
2. Detect body keypoints using MoveNet.
3. Extract relevant body landmarks.
4. Calculate relevant joint angles.
5. Compare the detected posture with reference pose templates.
6. Generate posture feedback based on the implemented scoring rules.

### Evaluated Pose Templates

- Savasana
- Balasana
- Viparita Karani

The current prototype uses controlled reference templates. Further calibration and evaluation using expert-labelled real-world pose data are required.

---

## API Performance Evaluation

The `/predict-domains` REST endpoint was evaluated using 60 sequential local requests.

| Performance Metric | Result |
|---|---:|
| Requests Completed | 60/60 |
| Mean Latency | 191.206 ms |
| P95 Latency | 231.617 ms |
| Throughput | 5.223 requests/second |
| CPU Utilisation | 86.37% of one core |
| Peak Memory | 781.75 MB |

These results represent a local REST API benchmark and should not be interpreted as production-scale or LangGraph orchestration performance.

---

## Project Deliverables and Documentation

The following section contains the academic documentation, presentations, research publication material, and project reports associated with AarogyaMitra.

**Replace each `PASTE_LINK_HERE` with the corresponding Google Drive, GitHub, or institutional document URL. Ensure that shared documents have the appropriate viewing permissions.**

| No. | Document / Deliverable | Link |
|---:|---|---|
| 1 | Complete Project Blackbook | [View Blackbook](https://docs.google.com/document/d/1F8LqPzgdp4-DY5ZBcnfOfMkTNUvToCdN5JbylOhult0/edit?usp=sharing) |
| 2 | Project Logbook | [View Logbook](https://docs.google.com/document/d/1AnpPvk9r8puBi5gxEd88-LsjJLLq4b61LJn-JVfEljY/edit?usp=sharing) |
| 3 | Video Presentation / Project Demonstration | [Watch Video Presentation](https://drive.google.com/drive/folders/1FbMWc_EcRkONfkWf--I0oJ1pR_Twpkg0?usp=sharing) |
| 4 | Review Presentation | [View Review Presentation](https://canva.link/851ebloi8eb3h9w) |
| 5 | Research Paper | [View Research Paper](https://drive.google.com/file/d/1tUmCj1IJ4U0_0E8VZlqQDo4m2bMZSed2/view?usp=sharing) |
| 6 | Research Paper Plagiarism Report | [View Plagiarism Report](https://drive.google.com/file/d/1CDmnhm8rpRShDhv8u8MPUhX-EfvY0P9v/view?usp=sharing) |


---

## Project Limitations

The current prototype has the following limitations:

- The machine learning model is trained using synthetic data rather than clinically collected patient data.
- Model evaluation currently uses an independent 80/20 holdout split.
- The yoga posture evaluation uses controlled reference templates and requires further real-world validation.
- Some pose-scoring calibration inconsistencies require investigation.
- The reported agent-routing evaluation is based on a limited set of manually designed scenarios.
- The reported API benchmark does not measure complete LangGraph orchestration performance.
- Clinical effectiveness and diagnostic accuracy have not been established.

---

## Future Scope

Potential future improvements include:

- Training and evaluating models using larger, diverse, ethically collected datasets.
- Performing cross-validation and external model validation.
- Improving yoga posture scoring through expert-labelled datasets.
- Expanding agent-routing and safety test coverage.
- Conducting dedicated LangGraph and context-layer performance evaluations.
- Improving crisis-risk detection and safety mechanisms.
- Integrating additional wellness data sources.
- Conducting usability studies and expert evaluations.
- Improving accessibility, scalability, and deployment reliability.

---

## Ethical Considerations and Disclaimer

AarogyaMitra is designed as a wellness awareness and support platform.

- Wellness scores are estimates, not clinical diagnoses.
- Questionnaire responses are self-reported screening information.
- AI-generated recommendations may contain errors and should be reviewed critically.
- The platform does not replace qualified mental-health professionals or emergency services.
- Sensitive wellness information should be handled with appropriate privacy, security, and access controls.

---

## Project Information

**Project Name:** AarogyaMitra – Understanding Mind and Body

**Project Category:** Agentic AI / Machine Learning / Computer Vision / Mental Wellbeing

**Project Type:** Capstone Project–II

**Academic Year:** 2026–27

**Department:** Computer Engineering

**Institution:** Vivekanand Education Society's Institute of Technology (VESIT)

---

## Acknowledgement

This project has been developed as part of the Capstone Project–II academic curriculum. We express our gratitude to our project guide, department faculty, and institution for their guidance and support throughout the development of AarogyaMitra.

---

<p align="center">
  <strong>AarogyaMitra – Understanding Mind and Body</strong><br/>
  <em>Bringing AI-driven insights closer to holistic well-being.</em>
</p>


### Launch Python ML Service (Optional)
From the root directory:
```bash
cd ml-service
python -m venv venv
# Windows:
.\venv\Scripts\activate
# Unix/macOS:
source venv/bin/activate

pip install -r requirements.txt
uvicorn app.main:app --port 8000 --reload
