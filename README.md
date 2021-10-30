# stratus-config

Configuration repo for [stratus](https://github.com/robertlestak/stratus).


## Identity Mapping Configuration

An example config block is:

```yaml
- source:
    id: "stratus-example@sandbox.iam.gserviceaccount.com"
    provider: "gcp"
    region: "us-central1"
  target:
    id: "arn:aws:iam::xxxxxx:role/stratus-example"
    provider: "aws"
    region: us-east-1
```

Identity Maps are configured in `configs/{folder_name}/{file_name}.yaml` files. The folder name should match the namespace/kv name it operates on for better management. The file name is arbitrary. Files are parsed into an array of config objects.
