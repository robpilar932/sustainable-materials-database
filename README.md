# Sustainable Materials Database

A collaborative database for evaluating, tracking, and comparing Environmental Product Declarations (EPDs) for construction materials. This system serves as a central, auditable knowledge base for sustainability projects, enabling informed material selection and life-cycle impact assessments.

## Purpose

Manually managing PDFs and spreadsheets for EPDs is inefficient, prone to errors, and difficult to share. This repository provides a structured, version-controlled system that standardizes extracted data, tracks changes, and implements a review process to ensure accuracy before new product data is added.

## Repository Structure

- `data/`: Stores structured product data, organized by product categories (e.g., `concrete/`, `insulation/`, `steel/`).
- `templates/`: Contains the data extraction template (`product-data-template.yml`) to ensure consistency.
- `docs/`: (Optional) Additional documentation and reference guides.

## Workflow for Adding a New Product

1. **Create an Issue**: Open a new issue with title "Evaluate EPD for [Product Name]" and include a link to the EPD document. Apply appropriate labels (e.g., `status: to-do`, `category: [material]`).

2. **Create a Branch**: From the issue, create a new branch named `feature/add-[product-name]`.

3. **Extract Data**: Navigate to the relevant category folder under `data/` and create a new YAML file using the template. Fill in the data extracted from the EPD.

4. **Commit and Push**: Commit the new file with a descriptive message.

5. **Open a Pull Request**: Open a PR to merge the branch into `main`. Reference the issue in the PR description (e.g., `Closes #1`).

6. **Review**: A reviewer examines the data against the template, asks clarifying questions, and approves the changes.

7. **Merge**: Once approved, the PR is merged (preferably with squash merge) and the issue is closed.

## Getting Started

To contribute, fork this repository, follow the workflow above, and submit a pull request.

## License

[Specify license, e.g., MIT]