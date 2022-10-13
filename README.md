<h1 align="center">
  Deploy static site to AWS
  <br>
</h1>

<h4 align="center">Batteries-included Github action that deploys a static site to AWS Cloudfront, taking care of DNS, SSL certs and S3 buckets</h4>

<p align="center">
  <img src="./images/flowchart.png">
</p>

## Usage
```yaml
- name: Deploy to AWS
  uses: sverigesradio/action-deploy-aws-static-site@v2
  with:
    AWS_ACCESS_KEY_ID: ${{ secrets.AWS_ACCESS_KEY_ID }}
    AWS_SECRET_ACCESS_KEY: ${{ secrets.AWS_SECRET_ACCESS_KEY }}
    region: eu-north-1
    certificate_arn: arn:partition:service:region:account-id:resource-type/resource-id
    domain: subdomain.example.com
    publish_dir: ./public
```
