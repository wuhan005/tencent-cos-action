> 官方的 GitHub Actions 年久失修，且质量极差，因此改一个自用。

# tencent-cos-action

Tencent Cloud COS GitHub Action.

## Inputs

### `secret_id`

**Required** Tencent Cloud secret id. Should be referred to a encrypted environment variable.

### `secret_key`

**Required** Tencent Cloud secret key. Should be referred to a encrypted environment variable.

### `cos_bucket`

**Required** COS bucket name.

### `cos_region`

**Required** COS bucket region.

### `local_path`

**Required** Local path to be uploaded to COS. Directory or file is allowed.

### `remote_path`

**Required** COS path to put the local files in on COS.

### `clean`

**Optional** Set to true for cleaning files on COS path which are not existed in local path. Default is false.

### `accelerate`

**Optional** Set to true for using accelerate domain to upload files. Default is false.

## Example usage

```
uses: wuhan005/tencent-cos-action@master
with:
  secret_id: ${{ secrets.TENCENT_CLOUD_SECRET_ID }}
  secret_key: ${{ secrets.TENCENT_CLOUD_SECRET_KEY }}
  cos_bucket: ${{ secrets.COS_BUCKET }}
  cos_region: ${{ secrets.COS_REGION }}
  local_path: build
  clean: true
  accelerate: true
```
