# Gsoc25
Performance Regression Publisher 

# Performance Regression Publisher

## Contact Information
- **Project Title:** Performance Regression Publisher
- **Email:** [khushi28132004@gmail.com](mailto:khushi28132004@gmail.com)
- **Mentor:** Dennis Korpel
- **Mentor’s Email:** [dkorpel@gmail.com](mailto:dkorpel@gmail.com)

## Personal Info
- **Name:** Khushi Shukla
- **Email:** [khushi28132004@gmail.com](mailto:khushi28132004@gmail.com)
- **GitHub:** [khushishukla2813](https://github.com/khushishukla2813) 
- **LinkedIn:** [Linkdin](https://www.linkedin.com/in/khushi1328/)
- **Website:** [Portfolio](https://khushishukla.vercel.app/)
- **Resume:**  [Resume](https://drive.google.com/file/d/1JxANhnL3-PjL-yofmSgqPtxvS3tYalip/view?usp=sharing)
- **Location:** India
- **Timezone:** IST (UTC +5:30)

## Student Affiliation
- **University:** Dr. Hari Singh Gour Sagar University, India
- **Degree:** BTech CSE (4th Semester)
- **Major:** Computer Science & Engineering
- **Expected Graduation:** 2027

## Brief Bio
I am Khushi Shukla, a second-year Computer Science Engineering student at Dr. Hari Singh Gour Sagar University, India, with a passion for compilers and performance optimization. My internship experience with LLVM and MLIR sparked my interest in compiler work, where I focus on optimizing performance, addressing time complexity issues, and improving compiler efficiency.

I’m also a developer, i develped bots for Telegram and WhatsApp, Apart from this I am proficient in Python, C, C++, Golang, D, and JavaScript, (MERN Stack), and I’m continuously learning new technologies to enhance my coding skills and contribute to real-world software solutions.

## Pull Requests

I’ve been actively contributing to several projects within the D programming language ecosystem, focusing on improving tools and documentation. Some of the pull requests I’ve worked on include:

- **dub-docs** #98
- **dub-registry** #587
- **dub-registry** #586
- **dub-docs** #97
- **dub-docs** #96
- **dmd** #21041
- **dmd** #20999
- **GSoC** #11

I’ve gained a deeper understanding of the D ecosystem and its challenges. As I continue to contribute, I’m excited to keep improving the tools, processes, and overall experience for everyone involved. My goal is to enhance both the performance and usability of D-related projects, and I’m eager to help drive meaningful improvements that make a difference to the community. I’m looking forward to continuing my journey within this vibrant ecosystem and growing alongside it!

## Project Description

## Abstract:
The D programming language lacks an automated performance regression testing system, making it difficult to verify compiler performance improvements. This project aims to create a bot that automates the monitoring of pull requests, collecting key performance metrics such as compile time, binary size, test suite runtime, and compiler size. It will also track regressions over time, providing transparent data for developers and ensuring performance integrity across changes.

## Background:
As the D compiler evolves, performance verification becomes crucial. Currently, pull requests claiming performance improvements are subject to manual verification, which is time-consuming and error-prone. By automating the process of performance tracking and regression testing, this project will streamline performance validation and help maintain high-quality standards for the D compiler.

## Project Proposal

### Overview:
This project aims to build a performance monitoring bot for the D compiler to provide insights into performance changes through automated testing. The bot will collect performance metrics and publish the results via GitHub Actions, making them easily accessible to contributors.

### Phase I: Basic Bot Implementation
  - Binary size for a basic "Hello World" program.
  - Compilation time of popular D projects.
  - Size of the D compiler itself.
  - Test suite runtime.
- **Objective:** Implement a bot that tracks basic performance metrics, publishes results on GitHub, and enables transparency in performance analysis.

### Phase II: Advanced Metrics and Stress Testing
- **Enhanced Testing:**
  - **Stress Tests:** Evaluate the compiler’s performance under heavy loads and large codebases.
  - **Advanced Metrics:** Memory usage, CPU load, disk I/O, page faults, and context switches during compilation.
  - **Historical Data:** Track trends and provide performance comparisons across D compiler versions.
- **Web Interface:** Develop a dashboard to visualize performance data, display trends, and offer insights.

## Enhancements for D Compiler Performance Monitoring

#### Real-time Performance Monitoring (Dashboard)
Implement a real-time dashboard to track compile time, binary size, and test suite runtime for each PR using D’s profiling flags and API integration for updates.

#### Granular Performance Analysis
Break down compile time into stages like preprocessing, parsing, and optimization by adding custom profiling hooks at key points in D's compilation pipeline.

#### Advanced Stress Tests
Stress test the compiler with multi-threading using D’s parallelism support, and use tools like `valgrind` or `perf` for CPU/memory profiling during compilation.

#### Automated Regression Detection
Use delta analysis to compare new performance data against a baseline and trigger alerts if performance degradation exceeds set thresholds.

#### GitHub Integration for Notifications
Automate GitHub comments on PRs, notifying maintainers of significant performance regressions based on compile time or binary size changes.

#### Historical Data Tracking and Trend Analysis
Track performance trends over time by storing metrics in a time-series database and visualizing them to compare compiler versions.

#### Testing Various Compiler Configurations
Measure performance across different compiler configurations like optimization levels, debugging flags, and link-time optimizations, automating tests in a CI pipeline.

#### Performance Threshold Alerts
Set up performance threshold alerts to flag PRs with regressions by defining sensible limits based on historical performance data.

#### Scalability and Parallelism
Design the bot to scale efficiently, managing multiple concurrent PRs and large codebases by utilizing cloud infrastructure for parallel processing.

#### User-friendly Environment (Dashboard)
Build a user-friendly web dashboard using React and D3.js to display performance data in clear, interactive graphs and tables for easy analysis.

### Additional Enhancements:
- **Benchmarking:** Integrate benchmarking tools to compare performance across different versions of the compiler.
- **Phobos Integration:** Test Phobos library performance as part of the overall benchmarking process.

### Current Implementation:
- **PerformanceBot Script:** A custom script that tracks essential performance metrics (such as compile time, binary size, and test suite runtime). This script automates the process of collecting performance data, runs predefined benchmarks, and display result on Dashboard.
![PerformanceBot in Action](https://raw.githubusercontent.com/username/repository/branch/src/Screen%20Recording%202025-03-23%20215643.mp4)



- **Manual Performance Testing:** Performance testing was done manually by running test files and scripts to measure compile time, binary size, and other relevant metrics. The results were then compared to baseline data to assess any regressions or improvements in performance.

| Test File                          | Compile Time (Before) | Compile Time (After) | Binary Size (Before) | Binary Size (After) |
|------------------------------------|-----------------------|----------------------|----------------------|---------------------|
| `hello.d` (No optimization)        | 0.425s                | 0.430s               | 1.3MB                | 1.3MB               |
| `hello.d` (With optimization)      | 0.496s                | 0.496s               | 1.3MB                | 1.3MB               |
| `hello.d` (With LTO optimization)  | 0.460s                | 0.460s               | 1.3MB                | 1.3MB               |
| `hello.d` (Parallel Build)         | 0.442s                | 0.442s               | 1.3MB                | 1.3MB               |
| `stress_test.d`                    | 0.547s                | 0.547s               | 1.3MB                | 1.3MB               |
| `large.d`                          | 0.417s                | 0.417s               | 1.3MB                | 1.3MB               |
| `multi-file test (3 files)`        | 0.004s                | 0.004s               | 1.3MB                | 1.3MB               |


- **Custom Script for Automation:** I developed a custom script to automate the performance data collection and reporting. This script runs performance benchmarks, compares results to baseline data, and automatically posts a comment on the PR with performance insights and alerts for any regressions.

   ![Custom Script Automation](src/Screenshot%202025-03-23%20223105.png)


## FlowChart:

### Performance Regression Testing Process
![image](https://github.com/user-attachments/assets/19ad9da1-c2fa-4e76-99e2-70642061721d)
This flowchart outlines the steps in the performance regression testing process, from conducting tests to storing results. It helps visualize how performance metrics are analyzed and reported.



### Overview of Performance Regression Analysis Approach
![image](https://github.com/user-attachments/assets/d7ba7b42-be6b-4816-a108-b18740680a23)

This flowchart breaks down the process of metric normalization, discretization, and report generation, helping track performance deviations and store results for future analysis.



### Performance Regression Testing Process
![image](https://github.com/user-attachments/assets/bb672eaf-15d3-4933-9cd2-64e22e00c99e)


This flowchart outlines the automated process of performance regression testing for the D compiler. It starts when a developer submits a pull request, triggering tests via GitHub Actions to evaluate performance metrics like compilation time, binary size, and memory consumption. Any regressions are flagged for review to ensure performance standards are maintained before merging.

### How it Helps:
- **Automates Testing:** Reduces manual checks, ensuring consistent and reliable performance tracking.
- **Informs Decisions:** Provides data-driven insights to assess whether a pull request improves or degrades performance.
- **Detects Regressions Early:** Flags performance issues early, preventing them from accumulating.
- **Improves Collaboration:** Enhances transparency with clear reports, improving communication among developers.
- **Supports Continuous Optimization:** Tracks performance trends to guide future improvements.
- **Simplifies Review:** Streamlines the review process with automated testing and performance reporting.

## Timeline

### Week 1:
I will set up the development environment and research the best method to implement a performance regression bot for the D compiler & implement the initial GitHub Action to trigger the bot and collect basic performance metrics like compile time and binary size.

### Week 2:
I will develop a reporting system to display collected metrics and document the setup process.

### Week 3:
I will test, refine, and optimize the bot for consistency and performance across multiple pull requests.

### Week 4:
I will expand the bot to collect additional performance metrics and implement stress tests for the compiler.

### Week 5:
I will create a storage solution to record historical performance data and begin visualizing trends.

### Week 6:
I will finalize the bot with stress testing, refine data visualization, and optimize performance.

### Week 7:
I will complete the final documentation, wrap up the project, and prepare a report on the outcomes.

## Commitments

During weekdays (Monday through Friday), I will dedicate 3-4 hours per day to the project. This schedule allows for regular progress and effective communication with my mentor. On weekends (Saturday and Sunday), I will extend my work hours to 7-8 hours per day to ensure steady progress and meet deadlines.

### Additional Information about the Timeline
The timeline is an approximate outline, and I will adapt it as needed during the pre-GSoC and community bonding phase. I can dedicate 25-30 hours per week throughout the summer, with the exception of the last month when my academic commitments begin. During this period, I can commit up to 15-20 hours per week, focusing on completing the project’s critical aspects before my classes start. I will allocate time for planning, learning, coding, testing, and documenting, ensuring that all documentation is done alongside development.

## Post GSoC Plans

I am committed to the long-term success of the Performance Regression Publisher project. While the main focus of this proposal is to automate performance testing for D compiler pull requests, I see opportunities to enhance the user experience. If time allows, I would explore enabling users to receive real-time performance alerts directly in their pull requests and developing a visual dashboard for easier trend analysis. This would further streamline the workflow and provide deeper insights into performance regressions.

- **Internship Project**: [IITH-Compilers/ml-llvm-project](https://github.com/IITH-Compilers/ml-llvm-project)
  - This is where I did my internship, focusing on compilers, ML compilers, and optimizations for ML codes using LLVM and MLIR.

- **Compiler Development**: [khushishukla2813/Compiler_](https://github.com/khushishukla2813/Compiler_)
  - This is the repository where I developed a multithreaded C compiler as part of my project work.

