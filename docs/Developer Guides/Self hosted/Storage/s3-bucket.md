---
sidebar_label: "S3 bucket"
title: "Configuring S3 Bucket as storage in Woofed CRM"
sidebar_position: 2
---

### Using Amazon S3

You can get started with [Creating an S3 bucket](https://docs.aws.amazon.com/AmazonS3/latest/gsg/CreatingABucket.html) and [Create an IAM user](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_users_create.html) to configure the following details.

Configure the following env variables.

```bash
ACTIVE_STORAGE_SERVICE='amazon'
S3_BUCKET_NAME=
AWS_ACCESS_KEY_ID=
AWS_SECRET_ACCESS_KEY=
AWS_REGION=
```

**Add CORS Configuration on your S3 buckets**

You need to configure CORS settings.

Refer to this link for more information: https://edgeguides.rubyonrails.org/active_storage_overview.html#cross-origin-resource-sharing-cors-configuration

To make CORS configuration changes on S3:

1. Go to your S3 bucket
2. Click on the permissions tab.
3. Scroll to Cross-origin resource sharing (CORS) and click on `Edit` and add the respective changes shown below.


```
[
  {
    "AllowedHeaders": [
      "*"
    ],
    "AllowedMethods": [
      "PUT",
      "POST",
      "DELETE",
      "GET"
    ],
    "AllowedOrigins": [
      "*"
    ],
    "ExposeHeaders": [
      "Origin",
      "Content-Type",
      "Content-MD5",
      "Content-Disposition"
    ],
    "MaxAgeSeconds": 3600
  }
]
```
