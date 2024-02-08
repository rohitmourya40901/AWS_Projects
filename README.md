# Static Website Hosting with Amazon S3

This project demonstrates the process of creating and hosting a static website using an Amazon S3 bucket. By following the steps outlined in this guide, you can quickly deploy a simple static website on Amazon Web Services (AWS).

## Table of Contents
- [Overview](#overview)
- [Prerequisites](#prerequisites)
- [Setup](#setup)
- [Usage](#usage)
- [Customization](#customization)
- [Contributing](#contributing)


## Overview

This project focuses on the hosting of a static website, perfect for showcasing portfolios, project documentation, or personal blogs. Amazon S3 is utilized for its simplicity, scalability, and cost-effectiveness in hosting static content.

## Prerequisites

Before you begin, ensure you have the following prerequisites:
- An AWS account
- AWS CLI installed and configured with necessary credentials
- Basic knowledge of HTML, CSS, and JavaScript for customizing your website

## Setup

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/yourusername/static-website-aws-s3.git
   ```

2. **Navigate to the Project Directory:**
   ```bash
   cd static-website-aws-s3
   ```

3. **Configure AWS CLI:**
   Ensure your AWS CLI is configured with the necessary credentials.

4. **Edit Website Content:**
   Modify the HTML, CSS, and JavaScript files in the `public` directory to customize your website.

5. **Create S3 Bucket:**
   Run the following AWS CLI command to create an S3 bucket for your website. Replace `your-bucket-name` with a unique name.

   ```bash
   aws s3 mb s3://your-bucket-name
   ```

6. **Upload Website Files:**
   Upload your website files to the S3 bucket.

   ```bash
   aws s3 sync public/ s3://your-bucket-name
   ```

7. **Set Bucket Policy:**
   Update the bucket policy to allow public access. Modify the `bucket-policy.json` file with your bucket name and execute the following command:

   ```bash
   aws s3api put-bucket-policy --bucket your-bucket-name --policy file://bucket-policy.json
   ```

8. **Enable Website Hosting:**
   Enable static website hosting on the S3 bucket.

   ```bash
   aws s3 website s3://your-bucket-name --index-document index.html --error-document error.html
   ```

9. **Access Your Website:**
   Once the setup is complete, your website will be accessible at the provided endpoint.

## Usage

Visit your website's endpoint to view your hosted static website. Share the URL with others to showcase your content.

## Customization

Feel free to customize the website content, style, and structure according to your preferences. Update the HTML, CSS, and JavaScript files in the `public` directory.

## Contributing

Contributions are welcome! Fork the repository, make your changes, and submit a pull request. Please follow the existing coding style and guidelines.

## OUTPUT 
