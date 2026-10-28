# Verify Repository Artifacts

The expected SHA-256 value for each published artifact is listed in [EVIDENCE_INDEX.md](EVIDENCE_INDEX.md). Run the command from the repository root and compare the complete output with the corresponding entry.

## Windows PowerShell

```powershell
Get-FileHash -Algorithm SHA256 -LiteralPath "relative/path/to/artifact"
```

## Linux or macOS

```sh
sha256sum "relative/path/to/artifact"
```

A match requires all 64 hexadecimal characters to be identical. The frozen H8-M result identity `547BD9E1E0DF965715E951234DC2A9FFDA422FF2163BA90ACD1F1CD154F005DF` identifies the original result file used to produce the sanitized H8-M evidence. That original result file is not included in this repository.
