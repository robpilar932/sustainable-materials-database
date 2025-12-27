# Documentation

This directory contains additional documentation for the Sustainable Materials Database.

## Overview

The Sustainable Materials Database is a version-controlled system for tracking Environmental Product Declarations (EPDs). It standardizes the extraction of key life-cycle impact indicators, enabling consistent comparison across products and materials.

## Data Schema

The data schema is defined in `templates/product-data-template.yml`. Each product entry includes:

- **Basic product information**: name, manufacturer, EPD program operator, declared unit, reference service life.
- **Life-Cycle Impact Assessment (LCIA) results**: Global warming potential (GWP), ozone depletion (ODP), acidification (AP), eutrophication (EP), photochemical ozone creation (POCP), abiotic depletion (fossil and elements), water use.
- **Additional metadata**: notes about the declared unit, data source, review status, review date, reviewer.

## Adding a New Product

### Step 1: Create an Issue
Open a new issue with the title "Evaluate EPD for [Product Name]". In the description, provide a link to the EPD document and any relevant notes. Apply labels:
- `status: to-do`
- `category: [material]` (e.g., `concrete`, `insulation`, `steel`)

### Step 2: Create a Branch
From the issue, create a new branch (e.g., `feature/add-product-name`). Use the GitHub UI or command line.

### Step 3: Extract Data
1. Navigate to the appropriate category folder under `data/`.
2. Create a new YAML file named after the product (e.g., `eco-struct-concrete-mix-c.yml`).
3. Copy the template from `templates/product-data-template.yml` and fill in the values from the EPD.

### Step 4: Commit and Push
Commit the file with a descriptive message (e.g., "Add data for Eco-Struct Concrete Mix-C").

### Step 5: Open a Pull Request
Open a pull request from your branch to `main`. In the PR description, reference the issue (e.g., `Closes #1`). Provide a brief summary of the data added.

### Step 6: Review
A reviewer will examine the data, compare it to the template, and may ask clarifying questions. Once satisfied, they will approve the PR.

### Step 7: Merge
After approval, merge the PR using a squash merge to keep the commit history clean. Close the associated issue.

## Review Guidelines

Reviewers should:
- Verify that all required fields are filled.
- Check that units match the declared unit in the EPD.
- Ensure numeric values are reasonable (e.g., not zero unless the EPD reports zero).
- Confirm that the reference service life aligns with the EPD.
- Ask questions if any data seems inconsistent.

## Contributing

We welcome contributions! Please follow the workflow above. If you have suggestions for improving the template or workflow, open an issue to discuss.

## License

This project is licensed under the MIT License - see the LICENSE file for details.