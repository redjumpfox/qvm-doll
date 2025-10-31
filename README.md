# Doll for QubesOS
qvm-doll

This script allow launching a qube from inside a VM.
Its focus is mostly disposable VM but any kind of VM can be launched, minus pure TemplateVM as this would very likely be a user mistake.

It automatically grants TCP permissions over the launched Qube, by design for simplicity of use with minimal needs for redundant policies.

usage:
`qrexec-client-vm dom0 local.custom.qvmdoll+somevm`

**The script requires execution permission to run**
`chmod +x /etc/qubes-rpc/local.custom.qvmdoll`

## Example Use case
This script was made with the purpose of launching several instances of chrome isolated in disposable VMs, and connecting to the remote debugging port of chrome using playwright.
