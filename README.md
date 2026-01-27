# Eye-Tracking Exam-Scenario Dataset (Anonymized)

This repository contains an anonymized eye-tracking dataset collected in a controlled, exam-like laboratory study. The dataset is released for methodological research on eye-tracking data preprocessing and time-series analysis and is used as a base dataset for the CUMULUS preprocessing benchmark.

The original study investigated gaze behavior under different task demands and permitted forms of cheating. All identifying information has been removed, and the dataset is provided solely for research and educational purposes.

---

## Experimental Overview

The data were collected during **four experimental sessions in 2023** with a total of **30 student participants** recruited from university lecture courses. Participants completed a **time-limited test consisting of five different task types** under controlled conditions.

The experiment was conducted in an eye-tracking laboratory equipped with stationary, monitor-mounted eye trackers. Participants were organized into groups of five. Within each group, four participants completed the tasks at eye-tracking workstations, while one participant acted as a supervisor (proctor), simulating a realistic examination setting.

Each group completed the full test within **20 minutes**, with individual tasks lasting between **2.5 and 4 minutes**.

---

## Task Design

The test consisted of **five distinct task types**, designed to elicit different cognitive and visual demands:

### 1. Definition Query Task
Participants were required to provide a concise definition of a given concept or term. This task assesses factual knowledge and understanding of domain-specific terminology.

### 2. Transfer Task
Participants applied previously acquired knowledge to solve a problem in an unfamiliar context. This task evaluates the ability to generalize and transfer knowledge to novel situations.

### 3. Multiple-Choice Task
Participants selected the correct answer from a set of multiple alternatives. This task type assesses recognition, comparison of options, and decision-making under time pressure.

### 4. Single-Choice Task
Participants selected one correct option from a limited set of answers. This task emphasizes precise decision-making with minimal ambiguity.

### 5. Application and Programming Tasks
The final task type consisted of two related subtasks requiring participants to apply conceptual knowledge and basic programming or problem-solving skills to practical scenarios. These tasks impose higher demands on working memory and attentional control.

---

## Permitted Cheating Conditions

To study the impact of external aids on task performance and gaze behavior, participants were allowed to choose between **three permitted cheating methods**:

- **Cheat Sheet:** Use of a prepared sheet containing task-relevant information.
- **Browser Access:** Use of a personal mobile device to access web resources.
- **Collaboration:** Verbal or non-verbal collaboration with neighboring participants.

After each task section, participants self-reported whether they used one of the cheating methods or did not cheat.

For the released dataset and the CUMULUS benchmark, cheating labels are **not required** and are not used for preprocessing evaluation.

---

## Experimental Procedure

Before the test, each participant completed an eye-tracker calibration procedure and provided informed consent for anonymous data usage. Tasks were presented using the iMotions software platform, which synchronized stimulus presentation with eye-tracking data recording.

Participants without eye-tracking devices received printed versions of the tasks and served as potential collaboration partners, further reinforcing the exam-like setting.

---

## Eye-Tracking Equipment

Two Tobii eye-tracking devices were used:

### Tobii Pro X3–120
- Sampling rate: 120 Hz
- Stationary, monitor-mounted device
- Infrared-based dark and bright pupil tracking
- High spatial and temporal precision

### Tobii Pro Nano
- Portable, compact eye tracker
- Infrared-based gaze estimation
- Single-camera system with embedded processing

Both devices were operated using the iMotions software platform.

---

## Recording and Filter Configuration

Key configuration parameters during data collection included:

- Screen resolution: 1920 × 1080 pixels
- Screen distance: 70 cm
- Monitor size: 27 inches
- Fixation detection: I-VT (Velocity-Threshold Identification) filter
- Velocity threshold: 30 deg/s
- Maximum gap length for interpolation: 75 ms
- Minimum fixation duration: 60 ms

These settings are device-typical and were kept consistent across sessions.

---

## Features / Columns

The dataset contains a rich set of gaze- and pupil-related features, including but not limited to:

- Gaze coordinates (left/right eye, combined gaze X/Y)
- Pupil diameter (left/right)
- Eye-to-screen distance
- Camera coordinates
- Validity indicators
- Interpolated gaze and distance values
- Gaze velocity and acceleration
- Saccade coordinates and duration
- Fixation duration and fixation coordinates

Exact column names may vary slightly across files.

---

## Missing Data and Artifacts

Missing values occur naturally due to blinks, temporary tracking loss, or calibration instability. The raw data intentionally preserve these characteristics to enable realistic preprocessing benchmarks. No synthetic corruption is applied in this repository.

---

## Intended Use

This dataset is intended for:

- Benchmarking preprocessing pipelines for eye-tracking time series
- Evaluating missing-value imputation, outlier handling, and normalization methods
- Methodological and reproducibility-focused research

It is **not intended for** fine-grained behavioral interpretation, clinical assessment, or geometry-dependent AOI/ROI analyses without additional metadata.

---

## Ethical Considerations

- All participants provided informed consent
- Data are anonymized and cannot be traced back to individuals
- The dataset complies with standard ethical requirements for anonymized behavioral research data

---

## Relation to CUMULUS

This dataset serves as the base data source for the **CUMULUS preprocessing benchmark**, which evaluates complete preprocessing pipelines under controlled corruption scenarios.

Repository:
https://github.com/eyetracking-data/CUMULUS

---

## License

This dataset is released for research and educational use only. See the repository license for details.
