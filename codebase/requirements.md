# *Preliminary Software Requirements Specifications (srs)*

## Functional Requirements 

Software must be able to ask the user for the type of training data that it requires, and then create the data based on the inputs from the user. 

The software must be able to display the data before and after the preparation. 

After the learning is created then the output and performance of the model must be show to the user. 

## Non-functional Requirements 

Requirements

    Number: 1
    Statement: The software must have Python installed.
    Evaluation Method: Verify Python installation using python --version or similar command.
    Dependency: None
    Priority: Essential
    Requirement revision history:
        Date: [Date]
        Change: Added requirement for Python installation.
        Reason: Python is essential for running the software.

Libraries Required

Before running the program, ensure the system has these libraries installed:

    csv
    matplotlib
    PIL
    pandas
    seaborn
    os
    time
    sys
    numpy
    sklearn.model_selection
    sklearn.linear_model
    sklearn.metrics
    sams_calibration_tool
 