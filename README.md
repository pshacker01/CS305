Artemis Financial - Secure Software Development ReadMe
Project Summary

Artemis Financial is a consulting company specializing in individualized financial planning, including savings, retirement, investments, and insurance. The company needed to modernize its software to ensure secure communication and data integrity for its clients. The primary issue Artemis Financial faced was the need to implement a file verification step using cryptographic hashing to verify data integrity. Additionally, the company wanted to enforce secure communication using HTTPS to prevent unauthorized access to sensitive client information.
Identifying Software Security Vulnerabilities

During the vulnerability assessment, I successfully identified security flaws and outdated dependencies that posed risks to the software’s integrity. One key strength was conducting an OWASP Dependency Check to find known vulnerabilities in third-party libraries. Additionally, I reviewed the software for missing security implementations, such as enforcing HTTPS and adding cryptographic checksum verification.

Secure coding is critical because it protects sensitive data from cyber threats, mitigates security breaches, and ensures compliance with regulatory standards. Implementing robust security measures strengthens the company’s credibility, fosters customer trust, and prevents financial and reputational damage from potential security incidents.
Challenges and Insights from Vulnerability Assessment

One of the main challenges in the vulnerability assessment was distinguishing between actual vulnerabilities and false positives. The OWASP Dependency Check flagged several issues, some of which did not pose a direct threat due to the way the software used those dependencies. To handle this, I created a suppression file to filter out false positives while maintaining the integrity of the security assessment.

Additionally, debugging SSL/TLS configurations required careful attention to ensure the application enforced HTTPS without breaking functionality. Understanding how Java Keytool generates and stores self-signed certificates was a crucial learning experience.
Enhancing Security Layers and Future Assessment Approaches

To increase security layers, I implemented the following:

    Enforced HTTPS communication by configuring SSL/TLS in the application properties.
    Implemented cryptographic hashing (SHA-256) to verify file integrity and prevent tampering.
    Used OWASP Dependency Check to identify and mitigate security vulnerabilities in third-party libraries.
    Configured a suppression file to exclude known false positives without ignoring real security threats.

In the future, I would use SAST (Static Application Security Testing) tools such as SonarQube and automated penetration testing tools to detect vulnerabilities dynamically. To decide on mitigation strategies, I would assess vulnerabilities based on CVSS (Common Vulnerability Scoring System) ratings and analyze exploitability.
Ensuring Functionality and Security of the Application

After refactoring the code, I followed a structured testing process to ensure security and functionality:

    Ran unit tests and integration tests to verify that the application functioned as expected.
    Conducted manual functional testing by executing API calls to confirm the checksum feature worked correctly.
    Performed a secondary dependency check to confirm that no new vulnerabilities were introduced.
    Tested SSL/TLS encryption using a web browser to ensure secure HTTPS communication.

By validating security measures post-refactoring, I ensured that Artemis Financial’s application met modern security standards without compromising usability.
Tools, Resources, and Best Practices for Future Use

Throughout the project, I relied on several tools and best practices, including:

    Java Keytool for generating self-signed SSL certificates.
    OWASP Dependency Check for identifying third-party library vulnerabilities.
    Spring Boot Security Best Practices for enforcing HTTPS and securing REST endpoints.
    Static Code Analysis using Maven plugins to ensure compliance with security guidelines.

These tools and practices will be valuable in future development projects where security is a priority.
Showcasing Work to Future Employers

This project is a strong demonstration of my ability to implement secure coding practices, identify vulnerabilities, and apply mitigation techniques effectively. Key aspects I can showcase to future employers include:

    My ability to secure a Spring Boot application by enforcing HTTPS and configuring SSL/TLS.
    Implementing cryptographic hash functions for data integrity verification.
    Conducting static code analysis using OWASP Dependency Check to identify security risks.
    Refactoring code while maintaining functionality and verifying security compliance.

This project highlights my skills in secure software development, cybersecurity best practices, and vulnerability mitigation—all essential for roles in software engineering and security-focused development.
