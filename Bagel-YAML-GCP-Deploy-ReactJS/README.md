# YAML that deploys React.JS website to GCP bucket
This YAML assumes you will be passing in some info for $_ENVIRONMENT and $_BUCKET_NAME. That info will usually be passed with Terraform code. 

Instead you could hard code in your bucket name and environment into the YAML.

## Terraform code that goes along with this YAML
- [Bagel Terraform Upload Site to GCP from Github Repo](https://github.com/BagelHole/Bagel-Terraform-Templates/tree/main/Bagel-Terraform-GCP-GitHub-Upload-Site)

## Bug
There is a bug when you first deploy using this YAML in cloud build in GCP. It will throw an error at you because there are no files in your created bucket to replace. This can be fixed by uploading any file to your bucket, and then every time after your cloud build should succeed. 

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License
[MIT](https://choosealicense.com/licenses/mit/)