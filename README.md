This is a reusable workflow to notarize a repository 
- using `vcn`
- using new ingest pipeline, ie. by generating vcn bom and posting this bom via curl directly to TC

The curl example:
```bash
curl -X 'POST' \
  'https://{domain}/dataservice/api/v1/sbom' \
  -H 'accept: application/json' \
  -H 'X-Content-Type: application/vnd.cyclonedx+json' \
  -H 'X-API-KEY: {secret}' \
  -H 'Content-Type: application/octet-stream'  \
  --data-binary '@{sbom_file}' | jq
```
