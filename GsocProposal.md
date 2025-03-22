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
- **Location:** India
- **Timezone:** IST (UTC +5:30)

## Student Affiliation
- **University:** Dr. Hari Singh Gour Sagar University, India
- **Degree:** BTech CSE (4th Semester)
- **Major:** Computer Science & Engineering
- **Expected Graduation:** 2027

## Brief Bio
I am Khushi Shukla, a second-year undergraduate student pursuing a degree in Computer Science Engineering at Dr. Hari Singh Gour Sagar University, India. I am passionate about enhancing software performance and contributing to open-source communities, with a focus on compilers, performance testing, and efficient coding practices.

I have hands-on experience in languages like Python, C, C++, Golang, D, and JavaScript, and I am actively involved in improving the D programming language ecosystem. I believe in the importance of clean, maintainable code, especially when working on complex systems such as compilers, and I am eager to apply my skills to improve software performance and optimize workflows.

Having contributed to various open-source projects, I am motivated by the impact of effective performance testing and optimization in real-world applications. I am excited to continue learning and contributing to the growth of the software development community.

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

### Abstract:
The D programming language currently lacks an automated performance regression testing system. When pull requests are made claiming improvements in compiler performance, there is often no easy way to validate whether the changes are genuinely beneficial. To address this, the goal of this project is to create an automated bot that monitors pull requests to the D compiler, analyzing its performance with and without the proposed changes. This bot will collect a variety of performance metrics, such as compile time, binary size, compiler size, and runtime of the test suite, providing reliable and transparent data for developers. Additionally, the system will maintain a history of performance metrics to help track regressions over time. This will greatly simplify the process of verifying performance improvements and ensure better quality control of the D compiler.

### Background:
As the D programming language continues to grow, maintaining high performance in its compiler is critical. However, verifying performance improvements in the absence of automated tools is challenging. Developers often submit pull requests claiming performance improvements, but it’s left to the reviewer to either take the claim at face value or manually test it. A system that automatically tracks and analyzes the performance of the compiler with and without the changes introduced in pull requests will save time and increase confidence in the integrity of the compiler’s performance. The idea behind this project is to implement a bot that continuously monitors performance regression, making it easier to validate performance improvements and detect regressions before they become a problem.

## Project Proposal

### Overview:
This project will be carried out in two phases, each building on the progress of the previous one. The first phase will focus on the initial implementation of the bot to monitor basic performance metrics, while the second phase will expand the functionality to include more comprehensive tests and a web interface for displaying the results.

### Phase I: Basic Bot Implementation
In this phase, the primary task will be to set up the bot to monitor pull requests and collect initial performance metrics. The metrics will include:
- Size of predefined binaries (e.g., a "Hello World" program).
- Compilation time of popular projects.
- Size of the compiler itself.
- Runtime of the test suite.

The bot will publish these results via GitHub Actions or a web interface, depending on the approach chosen during the initial planning. The goal of Phase I is to create a working bot that can reliably collect basic performance data from the D compiler.

### Phase II: Advanced Metrics and Stress Testing
In Phase II, the system will be enhanced with additional performance tests, such as stress tests for the compiler. More performance metrics will be collected, including memory usage and runtime analysis of larger projects. Additionally, the bot will be enhanced to store a history of performance data and present it via a web interface, making it easier for contributors to track performance trends over time.

The primary focus of Phase II will be on:
- Expanding the list of performance metrics.
- Adding stress tests for better insight into the compiler’s performance under heavy load.
- Building a web interface to display the results and historical performance data.

### Technologies:
- **GitHub Actions:** To automate performance tests and integrate with the existing D compiler workflow.
- **Web Development (HTML, CSS, JavaScript):** For developing a web interface to display performance data.
- **Python or Go:** To develop the bot that monitors pull requests and executes performance tests.
- **Performance Testing Tools:** To measure and track various performance metrics, such as compile time, memory usage, and binary size.

### Plan of Action:

#### Phase I:
- **Task 1:** Analyze the best way to publish results. This could be done through GitHub Actions or by sending data to a web interface. The choice will depend on the developer's preferences and the ease of implementation.
- **Task 2:** Develop the bot to monitor pull requests and track the time spent running the testing pipeline.
- **Task 3:** Implement basic performance tests, such as measuring compile time and binary size.
- **Task 4:** Set up a system to report and store these results, either through a GitHub action or a web interface.

#### Phase II:
- **Task 1:** Add stress tests to evaluate the compiler's performance under heavier loads.
- **Task 2:** Collect additional performance metrics, such as memory usage and the runtime of larger projects.
- **Task 3:** Build a web interface that presents historical performance data in an accessible way.
- **Task 4:** Test the system on various real-world pull requests to ensure its effectiveness and reliability.

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
