# ESP32 CSI-Based Helmet Detection Dataset

This dataset is collected using an ESP32 device for the purpose of estimating helmet usage and posture-based activity using Channel State Information (CSI) data.

## Dataset Structure

Each sample is a `.csv` file containing CSI readings for two categories:
- **helmet**
- **no_helmet**

For each category, samples are divided based on the posture and movement of the subject.

### Data Files

| Filename                     | Description                       |Approximate Samples (+- 1000 samples)|
|-----------------------------|-----------------------------------|---------|
| `helmet.csv`                | Base dataset with no sub-label    | 10,000  |
| `no_helmet.csv`             | Base dataset with no sub-label    | 10,000  |
| `helmet_sit_rotate.csv`     | Subject sitting and rotating      | 20,000  |
| `no_helmet_sit_rotate.csv`  | Same as above without helmet      | 20,000  |
| `helmet_sit_still.csv`      | Subject sitting still             | 20,000  |
| `no_helmet_sit_still.csv`   | Same as above without helmet      | 20,000  |
| `helmet_stand_rotate.csv`   | Subject standing and rotating     | 20,000  |
| `no_helmet_stand_rotate.csv`| Same as above without helmet      | 20,000  |
| `helmet_stand_still.csv`    | Subject standing still            | 10,000  |
| `no_helmet_stand_still.csv` | Same as above without helmet      | 10,000  |

## Notes

- Each CSV file contains time-series CSI readings.
- This dataset is intended for classification tasks such as:
  - Helmet vs. no helmet detection
  - Activity estimation (sit/stand, still/rotate) maybe, tho that's not the purpose rather than an additional task. The reason to have these was to have a cross domain dataset.
- All samples were collected in a controlled indoor environment.
