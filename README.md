# README

This script takes input some envs and based on the env values forms payload json files. Then uses these payload json files to create a snapshot. This script can be executed

## Env Table

Make changes to the ENV values only in config/es.env.sh

| ENV name | Description |
| - | - |
| repository_name | Name of the repository which exist or will be created |
| indices | Indices whose snapshot is to be created (eg. index1,index2 OR index-*) |
| partial | If aprtial snapshot is allowed(true or false) |
| include_global_state | If global cluster state is to be included (true or false) |
| ignore_unavailable | If ignore unavailable shards (true or false) |
| es_url | Url of the ES in the form http://host:port |
| s3_bucket_name | Name of the s3 bucket where snapshot is to be stored(ignore if repository already exist) |
| AWS_ACCESS_KEY | Do not set in File!!! Export elsewhere |
| AWS_SECRET_KEY | Do not set in File!!! Export elsewhere |

## Execute 

```
export AWS_ACCESS_KEY=******
export AWS_SECRET_KEY=******

chmod +x script.sh
./script.sh
```