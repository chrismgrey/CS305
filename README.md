# CS 305 Portfolio Artifact - Secure Software Practices (Artemis Financial)

## Overview

This repository contains my secure software artifact from CS 305. For this portfolio submission, I selected the Artemis Financial Practices for Secure Software report. The project focused on identifying security weaknesses in an existing application and refactoring it to meet modern secure development standards.

The objective was not just to make the application run, but to improve its integrity, encryption, and overall security posture using industry-recognized practices.


## Client Summary

The client in this project was Artemis Financial, a financial services company responsible for handling sensitive financial data. Because they work in a high-risk industry, protecting data integrity and securing communications was critical.

The primary issue that needed to be addressed was that the existing application lacked secure communication and proper data validation mechanisms. The system needed stronger hashing for integrity verification, encrypted communication using HTTPS, and vulnerability scanning to identify risks in third-party dependencies.


## What I Did Well in Identifying Vulnerabilities

One area I handled well was identifying insecure or outdated practices and replacing them with stronger alternatives. For example, I implemented SHA-256 hashing to generate secure checksums rather than relying on weaker or outdated algorithms. I also configured HTTPS using a self-signed certificate and keystore so that all communication runs over port 8443 instead of transmitting data in plain text.

It is important to code securely because financial systems are frequent targets. Even small weaknesses can lead to data exposure, regulatory consequences, and loss of customer trust. Secure coding adds value by reducing risk, protecting client information, and increasing confidence in the system’s reliability.


## Most Helpful or Challenging Part

The most helpful part of the vulnerability assessment process was running dependency-check and reviewing the report. It reinforced how many vulnerabilities can come from third-party libraries rather than just application code.

The more challenging portion was properly configuring SSL and generating the certificate using keytool. While the commands themselves are straightforward, understanding how the keystore integrates with the application configuration required careful attention to detail.


## Increasing Layers of Security

Security was added in layers throughout the project:

- SHA-256 hashing to protect data integrity
- HTTPS configuration using a generated certificate and keystore
- Refactored code to separate hashing logic into a controller
- Dependency scanning to identify known CVEs in external libraries

In the future, I would continue layering security through static analysis tools, automated CI pipeline scans, stronger certificate management practices, and potentially integrating authentication mechanisms.


## Ensuring Functionality and Security After Refactoring

After refactoring the code, I validated functionality by running the application and confirming that the hashing endpoint produced consistent SHA-256 checksums. I also verified that the application loaded securely in the browser and displayed an encrypted HTTPS connection.

To ensure no new vulnerabilities were introduced, I executed dependency-check and reviewed the results. This step confirmed that improvements did not introduce additional risk through external packages.


## Tools, Resources, and Practices Used

During this project, I used:

- Java keytool for certificate generation
- SHA-256 hashing for integrity validation
- HTTPS configuration through application properties
- OWASP dependency-check for vulnerability scanning
- Refactoring techniques to isolate security logic

These tools reflect common practices used in secure software development environments.


## What I Would Show Future Employers

From this assignment, I would show:

- My ability to refactor existing code to improve security
- Implementation of SHA-256 hashing for integrity validation
- Configuration of HTTPS and certificate-based encryption
- Experience running and interpreting dependency vulnerability scans
- Understanding of layered security principles

This artifact demonstrates that I understand not only how to make an application functional, but how to secure it using industry-aligned practices.
