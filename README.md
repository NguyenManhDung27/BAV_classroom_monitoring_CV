## BAV Classroom Monitoring Dataset (Banking Academy of Vietnam)

This dataset was collected and prepared by a research group at the Banking Academy of Vietnam (Học viện Ngân Hàng) to support computer vision research for assessing student engagement and activity in classroom settings. It is designed to help researchers develop and evaluate methods for detecting, quantifying, and reasoning about student attentiveness and participation from classroom imagery and associated annotations.

### Purpose

The primary goal of this dataset is to enable the development of computer vision models for tasks such as:
- Student presence and detection
- Posture and head-pose analysis
- Engagement / active participation estimation
- Visual Question Answering (VQA) and multimodal classroom understanding

Researchers can use this dataset to benchmark algorithms for automatic classroom monitoring, educational analytics, and tools that support instructors by providing objective signals of student engagement.

### Contents and structure

The repository contains the dataset split into common machine learning partitions and supporting annotation files. At the `Dataset for Detection/` you will find:

- `train/` — training images and its COCO-format annotation file `_annotations.coco.json`.
- `valid/` — validation images and its COCO-format annotation file `_annotations.coco.json`.
- `test/` — test images and its COCO-format annotation file `_annotations.coco.json`.
- `Question Dataset/` — supplemental JSON files intended for open-ended and single-choice VQA-style tasks (for example `Open_Ended_Question.json`, `Single_Choice_Question.json`, etc.).

Each `_annotations.coco.json` file follows the COCO annotation format: images, annotations (bounding boxes, category ids), and categories. Use standard COCO tools for parsing and evaluation.

### How to use

1. Inspect the annotations using COCO-compatible libraries (for example the Python `pycocotools` package) or your preferred CV framework.
2. For detection or localization tasks, use the COCO bounding-box annotations and standard evaluation metrics (mAP).
3. For engagement or activity estimation tasks, derive labels from the available annotations or the provided question files depending on the experimental setup.
4. For VQA experiments, the files inside `Question Dataset/` provide question/answer pairs aligned with images.

### Citation

If you use this dataset in published research, please cite the dataset and the associated work:

```bibtex
@inproceedings{vu2025exploring,
  title={Exploring the Application of Visual Question Answering (VQA) for Classroom Activity Monitoring},
  author={Vu, Sinh Trong and Pham, Hieu Trung and Nguyen, Dung Manh and Hoang, Hieu Minh and Le, Nhu Hoang and Pham, Thu Ha and Mai, Tai Tan},
  year={2025},
}
```

### License and contact

If a license file is not included in this repository, please contact the dataset owners or the project maintainer (see repository metadata) for permission and terms of use. This dataset was created for research purposes at the Banking Academy — please respect any non-commercial or attribution requirements specified by the authors.

For questions about the dataset, citation, or data access, please open an issue in the project repository or contact the authors listed in the citation.


_Prepared by the Banking Academy research team._
