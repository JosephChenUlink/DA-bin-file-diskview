# DA Drive Analyzer — Bin File Viewer

A browser-based viewer for DA Drive Analyzer `.bin` drive-health captures.
Supports **SATA**, **NVMe** and **SCSI/SAS**.

**Use it here:** https://josephchenulink.github.io/DA-bin-file-diskview/

---

## What it does

- Shows a capture's raw bytes alongside its decoded fields, record by record
- Decodes the file header — host, drive, capacity, and the record table
- Compares two captures field by field, highlighting every difference
- Sweeps a folder of captures, including subfolders and `.zip` archives
- Exports a formatted PDF report: cover, header page, one page per template

## Privacy

All processing happens in your browser. **No file content is uploaded, and no
server is contacted to read a capture.** Captures may contain drive
identifiers; note that serial numbers and host IDs in the header are stored
hashed or zeroed.

## Documentation

Click **Guide** in the toolbar for the full user guide.

## Support

Open an issue on this repository, or email joseph.chen@ulinktech.com.
Please include the version badge shown in the top right, the template number,
and the interface type. For layout or PDF problems, attach the exported PDF
rather than a screenshot.

---

## Licence

Copyright © 2026 ULINK Technology, Inc. All rights reserved.

This is **proprietary software**, not open source. You may use the hosted
viewer and keep the reports it produces. You may not copy, host, republish or
create derivative works from it — including its decoding tables and field
definitions — without written permission.

The source is visible at the address above because a web browser cannot run
code it has not received. That visibility is a technical necessity, not a
grant of licence. See [LICENSE](LICENSE) for the full terms and for the
third-party components (jsPDF, jsPDF-AutoTable, fflate), which carry their
own MIT licences.
