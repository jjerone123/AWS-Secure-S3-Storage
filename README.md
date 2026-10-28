AWS SECURE S3 STORAGE PROJECT
I CREATED AN AWS S3 BUCKET TO PRACTICE SECURE CLOUD STORAGE. I UPLOADED A TEST FILE, CHECKED ITS PERMISSONS, AND VERIFIED THAT PUBLIC ACSSES IS DENIED
THIS PROJECT DEMOSTRATES MY UNDERSTANDINGS OF AWS S3 , CLOUD STORAGE AND BASIC SECURITY TESTING 

## Security Controls Verified

- **Block Public Access:** Enabled on the bucket, so the bucket and its objects cannot be made public.
- **Encryption at rest:** Default encryption is SSE-S3 (Amazon S3 managed keys). SSE-C uploads are blocked.
- **Versioning:** Enabled. The first test upload shows a null version ID because it was uploaded before versioning was turned on. Later uploads have unique version IDs.
