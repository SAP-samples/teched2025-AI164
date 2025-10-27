# AI164 - Getting started with Joule: Provisioning and Contextualization

## Description

This repository contains the material for the SAP TechEd 2025 session called AI164 - Getting started with Joule: Provisioning and Contextualization.  

## Overview

Get hands-on experience with onboarding, provisioning, and contextualization for Joule technology. Guided by SAP experts, you can walk through the current steps involved in activating and grounding Joule in your business context—while learning what’s coming next to simplify and automate the process.

## Scenario

<img width="1736" height="843" alt="image" src="https://github.com/user-attachments/assets/75e3bc90-fab9-4805-bf2a-f0ed314bec7f" />


Imagine you are a system administrator. Your company is running multiple SAP systems, and you’ve just learned about Joule, the digital assistant designed to co-pilot your business. But how can you integrate Joule into your company’s landscape?

You would start by setting up an instance of Joule on SAP BTP and connecting it with your systems. This exercise will show you, in detail, how the provisioning process for Joule works. We’ll go through a simplified example of setting up Joule and Document Grounding, with the goal of connecting Joule to your company’s knowledge base.

For this purpose, we’ll use the Document Grounding Service that is set up alongside Joule. This service allows you to connect multiple knowledge sources, in particular Microsoft SharePoint, which is widely used across enterprises as a central repository for documents.

All of this setup takes place directly on SAP BTP, where you will have full control over the entire administration process from end to end. The final goal is to have Joule fully provisioned and connected to SharePoint, contextualized with your company-specific knowledge.

## Requirements

The requirements to follow the exercises in this repository are a general understanding of concepts like BTP administration, system integrations and SAP Joule.

## Exercises

- [Exercise 1 - Prepare the BTP Subaccount](exercises/ex1/)
    - [Step 1 - Log in to BTP](exercises/ex1#step1)
    - [Step 2 - Create a Subaccount](exercises/ex1#step2)
    - [Step 3 - Assign Entitlements to your Subaccount](exercises/ex1#step3)
    - [Step 4 - Establish Trust to the Custom Application IAS Tenant](exercises/ex1#step4)
    - [Summary](exercises/ex1#summary)
- [Exercise 2 - Run the Joule Booster](exercises/ex2/)
    - [Step 1 - Start the Booster](exercises/ex2#step1)
    - [Step 2 - Check Prerequisites](exercises/ex2#step2)
    - [Step 3 - Set Up Subaccount](exercises/ex2#step3)
    - [Step 4 - Select Integrations](exercises/ex2#step4)
    - [Step 5 - Select Capabilities](exercises/ex2#step5)
    - [Step 6 - Set Up Integrations](exercises/ex2#step6)
    - [Step 7 - Review and Execute](exercises/ex2#step7)
    - [Summary](exercises/ex2#summary)
- [Exercise 3 - Set Up Document Grounding](exercises/ex3/)
    - [Step 1 - Create Destination](exercises/ex3#step1)
    - [Step 2 - Create Document Grounding Service](exercises/ex3#step2)
    - [Step 3 - Prepare Key and Certificate File](exercises/ex3#step3)
    - [Step 4 - Set Up Bruno](exercises/ex3#step4)
    - [Step 5 - Execute API Calls](exercises/ex3#step5)
    - [Summary](exercises/ex3#summary)
- [Exercise 4 - Test Joule Standalone](exercises/ex4/)
    - [Step 1 - Log In to Joule](exercises/ex4#step1)
    - [Step 2 - Create a Role Collection and Assign it to Your User](exercises/ex4#step2)
    - [Step 3 - Log In to Joule Again and Start Testing](exercises/ex4#step3)
    - [Summary](exercises/ex4#summary)
  
 

## Contributing
Please read the [CONTRIBUTING.md](./CONTRIBUTING.md) to understand the contribution guidelines.

## Code of Conduct
Please read the [SAP Open Source Code of Conduct](https://github.com/SAP-samples/.github/blob/main/CODE_OF_CONDUCT.md).

## How to obtain support

Support for the content in this repository is available during the actual time of the online session for which this content has been designed. Otherwise, you may request support via the [Issues](../../issues) tab.

## License
Copyright (c) 2024 SAP SE or an SAP affiliate company. All rights reserved. This project is licensed under the Apache Software License, version 2.0 except as noted otherwise in the [LICENSE](LICENSES/Apache-2.0.txt) file.
