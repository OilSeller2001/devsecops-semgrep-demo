# Simple DevSecOps Demo

This is a basic DevSecOps demonstration project designed to showcase:

- A simple Python script (`trigger.py`) containing an intentional vulnerability
- GitHub Actions workflow for automated security scanning using Semgrep
- Automation of security checks on every push or pull request

## Project Structure

- `trigger.py`: A minimal Python script with a simple vulnerability (`eval()` usage) for testing.
- `.github/workflows/semgrep.yml`: GitHub Actions workflow to automatically scan code with Semgrep.

## How It Works

1. When code is pushed to the `main` branch or a pull request is opened, GitHub Actions triggers Semgrep.
2. Semgrep scans the codebase for security vulnerabilities based on predefined rule sets.
3. Scan results are shown in the GitHub Actions workflow logs.

## Purpose

This project demonstrates how to integrate **static application security testing (SAST)** into the **CI/CD pipeline** early in the development process ("shift-left" security).

## Future Improvements

- Add additional security tools (e.g., Bandit for Python, Trivy for container scanning)
- Expand the Python example to include different types of vulnerabilities
- Introduce containerization and infrastructure-as-code (IaC) scanning
