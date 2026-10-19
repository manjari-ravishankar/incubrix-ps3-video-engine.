
# IncuBrix PS3 — Test Pack

## 1. Test Environment

- Application: FastAPI
- Local development URL: http://127.0.0.1:8000
- API documentation: http://127.0.0.1:8000/docs

## 2. Test Cases

| ID | Test | Expected Result | Observed Result |
|---|---|---|---|
| TC-01 | Open `/docs` | API documentation loads | Passed during local testing |
| TC-02 | Submit a valid script to `/api/v1/broll/jobs` | Job ID and status returned | HTTP 202 and `voiceover_ready` observed |
| TC-03 | Open the returned audio URL | MP3 is accessible | MP3 downloaded successfully |
| TC-04 | Check generated timeline JSON | Timeline file exists and contains scene data | File existence observed; content needs review |
| TC-05 | Check generated SRT captions | Caption file exists | File existence observed |
| TC-06 | Open generated MP4 | Video plays correctly | Playback and synchronization need verification |
| TC-07 | Submit invalid input | Appropriate validation error returned | Not yet verified |

## 3. Evidence Locations

Local project outputs were found under:

- `outputs/voiceovers/`
- `outputs/timelines/`
- `outputs/captions/`
- `outputs/videos/`

## 4. Known Limitations

- Real B-roll footage selection and integration are not confirmed as implemented.
- Invalid-input handling and full video synchronization require additional tests.
- The local API is not a publicly accessible live demo.

## 5. Test Execution Record

Record the test date, environment, exact input, actual output, and pass/fail status when each test is executed. Do not mark untested cases as passed.
