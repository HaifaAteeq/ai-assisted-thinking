# Test Session: ChatGPT Free + Protocol v3.0/v3.1

## Session Info
- **Model:** ChatGPT (Free)
- **Protocol:** v3.0 and v3.1
- **Topic:** NumPy
- **Date:** February 2026
- **Result:** ❌ FAILED

## What Went Wrong
| Expected | Actual |
|----------|--------|
| Ask language/time/energy first | Skipped or combined |
| Show example, then ask | Explained first |
| ONE question per response | Sometimes multiple |

## Root Cause
- Free models have shorter context windows
- Protocol v3.0/v3.1 wasn't strict enough
- ChatGPT defaults to explaining

## Lesson Learned
Led to v3.2 development with stricter rules.
