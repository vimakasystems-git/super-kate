# Identifying Super Kate usage

This project publishes a cooperative, machine-readable identification method.

## Markers

An AI or code scanner can look for:

- super-kate-license.json
- Super Kate
- LicenseRef-Super-Kate-Community-1.0
- Vimaka Sistemas Inteligentes
- package, import, namespace, or build metadata containing super-kate

The canonical metadata is in super-kate-license.json. Projects that
redistribute or embed Super Kate should preserve that file and the license
notice.

## Example scan

    rg -n -i --hidden --glob '!node_modules' 'super[-_ ]kate|LicenseRef-Super-Kate-Community-1.0|Vimaka Sistemas Inteligentes' .

## Limits

This is a transparent, cooperative identification method. It is not hidden
telemetry, does not phone home, and cannot reliably detect code that has been
renamed, rewritten, or stripped of its notices. It should be used to flag
possible usage for human review, not as conclusive proof of copying or
commercial use.
