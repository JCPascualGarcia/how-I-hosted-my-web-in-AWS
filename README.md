# how-I-hosted-my-web-in-AWS

Descripción de todos los servicios usados para alojar mi web en AWS usando una distribución de CloudFront, un dominio de Route53 y certificados de ACM

Description of all the services used to host my web in AWS using a CloudFront Distribution, a Route53 domain and ACM certificates

Here's a comprehensive summary of your complete infrastructure setup for juan-carlos-pascual-garcia.com:

🏗️ Complete Infrastructure Summary

🌐 Domain & DNS (Route 53)
Domain: juan-carlos-pascual-garcia.com
Hosted Zone ID: ******22063ASD9J5UW05NV
Type: Public hosted zone (internet-accessible)
DNS Records: 7 total records configured
Nameservers:
ns-482.awsdns-60.com
ns-1775.awsdns-29.co.uk
ns-1263.awsdns-29.org
ns-585.awsdns-09.net
Status: ✅ Properly configured with AWS Route 53

📦 S3 Storage
Primary Bucket: juan-carlos-pascual-garcia.com
Region: eu-west-1 (Ireland)
Created: October 21, 2025
Configuration:
✅ Static website hosting: Disabled (secure setup)
✅ Public access: Blocked (secure)
✅ Versioning: Enabled
✅ Encryption: AES256 server-side encryption
✅ Object ownership: BucketOwnerEnforced
Access: Private (only accessible via CloudFront)

🚀 CloudFront CDN
Distribution ID: *****4B6P7I56
Domain: *****ulm6q2f7.cloudfront.net
Status: ✅ Working and properly configured
Origin Configuration:
Origin: S3 bucket (secure REST API endpoint)
Access Method: Origin Access Control (OAC) - Secure
Protocol: HTTPS supported
Region: Managed from us-east-1 (required for CloudFront)

🔒 Security Configuration
SSL/TLS Certificates: ACM certificates configured
✅ DNS validation records present in Route 53
✅ Supports both root domain and www subdomain
Access Control:
✅ Origin Access Control (OAC): Prevents direct S3 access
✅ Private S3 bucket: Only CloudFront can access content
✅ HTTPS: Secure connections supported
🔗 DNS Routing
Root domain (juan-carlos-pascual-garcia.com):
✅ Points to CloudFront distribution
✅ Both IPv4 (A) and IPv6 (AAAA) records configured
WWW subdomain (www.juan-carlos-pascual-garcia.com):
✅ CNAME record redirects to root domain
Certificate validation:
✅ ACM validation CNAME records present
📊 Infrastructure Architecture Flow
Internet Users
       ↓
Route 53 DNS (juan-carlos-pascual-garcia.com)
       ↓
CloudFront Distribution (duhbeulm6q2f7.cloudfront.net)
       ↓ (via OAC - secure)
S3 Bucket (juan-carlos-pascual-garcia.com)

🎯 Key Benefits of Your Current Setup
🔒 Security:
Private S3 bucket with OAC
HTTPS encryption
No direct S3 access possible

⚡ Performance:
Global CloudFront CDN
Edge caching worldwide
IPv6 support

💰 Cost Optimization:
Reduced S3 data transfer costs
CloudFront caching reduces origin requests

🛡️ Reliability:
AWS global infrastructure
Automatic failover capabilities
99.99% uptime SLA

✅ Current Status: FULLY OPERATIONAL
Your infrastructure is now properly configured with:

✅ Secure S3 origin with OAC
✅ Working CloudFront distribution
✅ Proper DNS routing
✅ SSL certificate validation
✅ Best security practices implemented

This is a production-ready, secure, and scalable web hosting setup following AWS best practices! 🎉




