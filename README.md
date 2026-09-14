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

## Reference specifications (for developers)

The decoding tables follow the ATA (ACS), SCSI (SPC/SBC), NVMe and OCP
specifications. Those documents are kept in the private repository
`JosephChenUlink/ULINK-Storage-Specs`, shared by every ULINK storage project.
This repository does not mount it as a submodule because the viewer is served
by GitHub Pages, whose branch build fails on a private submodule. Clone it
next to this repository instead:

```
git clone https://github.com/JosephChenUlink/ULINK-Storage-Specs
```

Cite specifications by document and section (for example "ACS-7 7.12",
"NVMe Base 2.3 5.16"), never by file path.

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
