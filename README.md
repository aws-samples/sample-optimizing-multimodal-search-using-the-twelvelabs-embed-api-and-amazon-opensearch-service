# Optimizing Multimodal Search Using the Twelve Labs Embed API and Amazon OpenSearch Service

A solution for implementing advanced video search capabilities by combining Twelve Labs' Embed API with Amazon OpenSearch Service. This integration enables sophisticated multimodal search across video content using AI-powered video understanding and vector search capabilities.

**Disclaimer:** Sample code, software libraries, command line tools, proofs of concept, templates, or other related technology are provided as AWS Content or Third-Party Content under the AWS Customer Agreement, or the relevant written agreement between you and AWS (whichever applies). You should not use this AWS Content or Third-Party Content in your production accounts, or on production or other critical data. You are responsible for testing, securing, and optimizing the AWS Content or Third-Party Content, such as sample code, as appropriate for production grade use based on your specific quality control practices and standards. Deploying AWS Content or Third-Party Content may incur AWS charges for creating or using AWS chargeable resources, such as running Amazon EC2 instances or using Amazon S3 storage. This application uses various AWS services and there are costs associated with these services after the Free Tier usage - please see the AWS Pricing page for details. You are responsible for any AWS costs incurred. No warranty is implied in these examples.

## Overview

This project demonstrates how to:
- Generate rich vector embeddings from video content using Twelve Labs Embed API
- Store and index video embeddings in Amazon OpenSearch
- Perform multimodal semantic search across video libraries
- Enable sophisticated video discovery and analysis

#### Architecture Overview 

The following diagram provides an overview of the architecture and the steps followed to 
- Embedding a video file using Twelve Labs Embed API
- Ingesting video embeddings to Amazon OpenSearch
- Users can search the video embedding using Text, Audio, or Image.
- User uses Twelve Labs Embed API to create the corresponding embeddings.
- Searches video embeddings in Amazon OpenSearch and retrieves the corresponding vector.

![Figure 1: Architecture for Twelve Labs Embed API and Amazon OpenSearch use case](./images/twelvelabsAndOpenSearchArchitecureDiagram.png)

## Features

- **Multimodal Video Understanding**
  - Process visual expressions, body language, spoken words, and context
  - Generate 1024-dimensional vector embeddings

- **Advanced Search Capabilities** 
  - Semantic search using text queries
  - Visual similarity search
  - Combined multimodal search

- **Scalable Architecture**
  - Serverless deployment on AWS
  - Vector storage and indexing with OpenSearch
  - Integration with Twelve Labs

## Prerequisites
  - Confirm that you have an [AWS account](https://docs.aws.amazon.com/accounts/latest/reference/manage-acct-creating.html)
  - Create a [Twelve Labs account](https://auth.twelvelabs.io/u/signup/) as it will be required to get the API Key. Twelve labs offer free tier [pricing](https://www.twelvelabs.io/pricing) but you can upgrade as per your requirement.
  - Have an Amazon OpenSearch domain. If you do not have an existing domain, you can create one using the steps outlined in our public documentation for [Creating and Managing Amazon OpenSearch Domain](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/createupdatedomains.html). Ensure that OpenSearch domain is accessible from your python environment. You can also use [Amazon OpenSearch Serverless](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/serverless.html) for this use case and update the interactions with OpenSearch serverless using [AWS SDKs](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/serverless-sdk.html).

## Running the notebook
Follow the steps in the `Twelve_Labs_Opensearch.ipynb` notebook to create embedding and perform search.

## Authors
Contributor names and info

  - James Le, Head of Developer Experience, TwelveLabs
  - Gitika Vigh, Senior WW Data & AI PSA, AWS
  - Kruthi Rao, Partner Solutions Architect, AWS
    
## License
Copyright 2024 Amazon.com, Inc. or its affiliates. All Rights Reserved.

This library is licensed under the MIT-0 License. See the LICENSE file.

