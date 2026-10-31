# RG HotelOS — releases

Installers for **RG HotelOS**, the offline-first hotel and restaurant system by RG Devs.
This repository holds releases only; the source code is private.

## Installing at a hotel

Download `RG-HotelOS-Setup-x.y.z.exe` from the latest release and run it **as administrator** on the hotel's
server PC (Windows 10 or 11). Windows SmartScreen may show "unknown publisher" until the installer is code-signed:
choose *More info → Run anyway*. A licence from RG Devs is needed to take transactions.

## Automatic updates

Each release also carries `latest.json`: a manifest signed with RG Devs' Ed25519 key, holding the installer's
version, SHA-256 and size. Hotel servers read
`https://github.com/kenrodgersutugi-tech/rg-hotelos-releases/releases/latest/download/latest.json`,
refuse anything not signed by RG Devs or not matching its checksum, and install only at night when the hotel is quiet.
Pre-releases (release candidates) are not offered to hotels automatically.

Support: RG Devs.
