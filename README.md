# Evaluating-a-Manufacturing-Process

# Overview

This project focuses on improving the monitoring and control of a manufacturing process by implementing Statistical Process Control (SPC). SPC is a data-driven method used to ensure the consistency and quality of manufactured parts by identifying when a process requires adjustment. The analysis aims to detect parts falling outside acceptable thresholds and improve overall production efficiency.

# Objectives

- Define acceptable height limits for manufactured parts using statistical formulas.
- Identify parts produced outside these control limits to flag potential issues in the process.
- Use SQL techniques to automate monitoring and enable early detection of inconsistencies.
- Support manufacturing teams in enhancing process control and product quality.

# Data Source

The dataset is accessed through DataCamp’s DataLab environment and is stored in a SQL table named manufacturing_parts. It includes:
- item_no – Unique identifier for each item
- length, width, height – Physical dimensions of the item
- operator – The machine or operator responsible for the part
The dataset contains 500 records.

# Tools Used

- DataLab – For interactive analysis within a notebook environment
- PostgreSQL – For performing data queries, aggregations, and statistical calculations
- SQL window functions – To calculate running averages, standard deviations, and apply control limits

# Insights

- SPC uses the average and standard deviation of item height to calculate the Upper Control Limit (UCL) and Lower Control Limit (LCL):
  - UCL = avg_height + (3 * stddev_height / √5)
  - LCL = avg_height − (3 * stddev_height / √5)
- These thresholds help to highlight deviations that may indicate equipment faults or process instability.
- Visualising the height distribution across sequential parts reveals fluctuations and potential outliers.

# Key Findings

- Several parts fall outside the calculated control limits, particularly around certain row intervals, suggesting variability in output.
- Most values remain within tolerance, indicating the process is generally stable but prone to occasional deviations.
- Some operators may require further investigation or recalibration of equipment due to irregularities in specific batches.

# Recommendations

- Implement real-time SPC dashboards to monitor control limits continuously and flag deviations as they occur.
- Investigate outliers by analysing the equipment or operator associated with affected items.
- Schedule preventative maintenance where irregular output is observed, particularly for machines producing out-of-spec parts.
- Expand SPC analysis to include other dimensions such as length and width for more holistic quality assurance.
