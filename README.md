# DevOps Portfolio – Static Website on AWS S3

## What I customized
- Rebranded the HTML to **Tosin Sanda** (name, tagline, colors).
- Updated skills, certifications, and projects list.
- Added contact email and LinkedIn link.

## S3 static website
**URL:** (http://tosinsanda-portfolio.s3-website-us-east-1.amazonaws.com)  
Static hosting enabled with `index.html` as root document.

## Bucket policy
```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "AllowPublicRead",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::<tosinsanda-portfolio>/*"
    }
  ]
}
