# gpio-roof-home — Historical roof-driver experiment

> **Status: historical / unverified. Do not use as the RETLU observatory roof controller.**

This repository contains an early Odroid/Raspberry Pi GPIO-controlled roll-off-roof driver with a home sensor. The tracked repository is minimal: a README and the `odroid_roof_edited` source file. No test suite or current commissioning evidence is recorded here.

This code is retained as a historical reference only. It must not be assumed to provide the safety behaviour required by the RETLU observatory.

## RETLU safety requirements

A future RETLU roof controller must be designed and validated against the current RETLU safety contract, including:
- independent and reliable open/closed position sensing
- bounded opening and closing timeouts
- fail-safe handling of missing, stale or contradictory sensor feedback
- rain/weather response and safe telescope parking coordination
- physical interlocks and emergency stop
- explicit locks and prevention of unsafe concurrent actions
- fault-injection and physical commissioning tests

A home sensor alone is not sufficient evidence that the roof is safely open or closed. A successful GPIO command is not proof of physical movement or final position.

## Use

Do not connect this historical driver to the production observatory or use it for unattended roof movement. Any reuse requires a fresh code review, hardware review, safety design and tests against the current RETLU Safety Contract before it can be considered.
