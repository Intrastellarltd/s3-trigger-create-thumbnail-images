# Using an Amazon S3 trigger to create thumbnail images - Terraform

## Video

## Introduction

In this tutorial a Lambda function that resizes images added to an Amazon Simple Storage Service (Amazon S3) bucket will be created. When an image file is added to a bucket, Amazon S3 invokes the Lambda function. The function then creates a thumbnail version of the image and outputs it to a different Amazon S3 bucket.

## Problem Statement and Solution

- Create source and destination Amazon S3 buckets and upload a sample image.

- Create a Lambda function that resizes an image and outputs a thumbnail to an Amazon S3 bucket.

- Configure a Lambda trigger that invokes the function when objects are uploaded to the source bucket.

## Architecture Diagram

![Deploy NextJS App to S3 and CloudFront with Github Actions - Terraform](/architecture-diagram/S3TriggerToCreateThumbnailImagesTerraformDark.png)

## Project Walkthrough

- **s3 Bucket**
  - Create two Amazon S3 buckets
  - Upload a test image to the source bucket

- **Lambda Function**
  - Create a permissions policy
  - Create an execution role
  - Create the function deployment package
  - Create the Lambda function

- **Trigger**
  - Configure Amazon S3 to invoke the function

- **Test**
  - Test Lambda function with a dummy event
  - Test with trigger
