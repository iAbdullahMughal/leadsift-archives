# leadsift-archives

Password-protected release archives of the [LeadSift](https://github.com/iAbdullahMughal/leadsift) Windows executable.

**No source code. No tarballs. Only the built exe, encrypted.**

## How it works

- Every archive contains a single `LeadSift.exe`, compressed with 7-Zip as an **AES-256 encrypted `.zip`**.
- The archive password is the **full Git commit SHA** of the `leadsift` commit that produced the build — recorded in each archive's commit message as `from leadsift@<sha>`.
- Naming: `LeadSift-<release tag>-<short commit sha>.zip`

## Extract

Install [7-Zip](https://www.7-zip.org/), then:

    7z x LeadSift-v1.0.3-abc1234.zip -p<FULL_COMMIT_SHA>
