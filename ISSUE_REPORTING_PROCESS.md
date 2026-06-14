# Issue Reporting Process
This repository enforces a structured bug reporting workflow for LineageOS issues using a GitHub issue form and automation.

## 1) Before reporting
- Check existing issues for duplicates.
- Read the official bug reporting instructions: https://wiki.lineageos.org/how-to/bugreport

## 2) What this tracker accepts
The tracker is configured for **Bug Report** submissions only.

Not accepted here:
- Bugs from unofficial builds or non-official download sources
- Missing builds
- Website issues
- Device support requests
- Feature requests

For general help/support, users are directed to community channels:
https://lineageos.org/community

## 3) Required report fields
The Bug Report form requires:
- Device codename (e.g., `mako`, not marketing name)
- Exact LineageOS version (not “latest”)
- Build date in `YYYYMMDD`
- Kernel version
- Expected behavior
- Current behavior
- Steps to reproduce
- Confirmation that bugreport directions were read

Optional fields include baseband version, system modifications, and possible solution.

## 4) Automated validation and triage
When an issue is opened (or reopened via `/reopen`), automation parses and validates the form:
- Issue must match the expected template format
- Device codename must be a supported codename
- Reported LineageOS version must match the supported version for that device
- Build date must match valid date format (`YYYYMMDD`, with optional suffix)

If validation succeeds:
- The issue is kept open
- Labels are applied (including device and version labels)
- Device maintainers are auto-assigned when possible

## 5) What happens on invalid reports
If the template is not used or validation fails:
- A bot comment explains what is wrong
- The issue is automatically closed
- Reporter is instructed to fix details and comment `/reopen` to trigger validation again

## 6) Reopen flow
Closed issues can be retried by the original reporter using:
- `/reopen`

This triggers the same parsing/validation workflow and reprocesses labeling/assignment if the report is corrected.
