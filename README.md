AWS SECURE S3 STORAGE PROJECT
I CREATED AN AWS S3 BUCKET TO PRACTICE SECURE CLOUD STORAGE. I UPLOADED A TEST FILE, CHECKED ITS PERMISSONS, AND VERIFIED THAT PUBLIC ACSSES IS DENIED
THIS PROJECT DEMOSTRATES MY UNDERSTANDINGS OF AWS S3 , CLOUD STORAGE AND BASIC SECURITY TESTING 

## Security Controls Verified

- **Block Public Access:** Enabled on the bucket, so the bucket and its objects cannot be made public.
- **Encryption at rest:** Default encryption is SSE-S3 (Amazon S3 managed keys). SSE-C uploads are blocked.
- **Versioning:** Enabled. The first test upload shows a null version ID because it was uploaded before versioning was turned on. Later uploads have unique version IDs.


## IAM Access Control (Least Privilege)

- **IAM user:** s3-training-user, a test user created to practice read-only access.
- **Group:** s3-view-only. The user receives permissions through this group.
- **Policy:** s3-portfolio-read-only-policy allows only s3:GetObject and s3:ListBucket on this bucket and the objects inside it.
- **No write or delete access:** The policy contains no PutObject or DeleteObject permissions.

## Testing and Validation

- Used the IAM Policy Simulator on s3-training-user.
- **s3:GetObject:** Allowed (explicit allow in the group policy).
- **s3:PutObject:** Implicitly denied (no matching allow statement).
- Result: the user can read objects but cannot upload or change them.
