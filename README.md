Here's the updated version with the post scriptum at the end:

# Usermode VALORANT Injector via SetWindowHookEx

An updated fork of [DrNseven's hookloader](https://github.com/DrNseven/hookloader), a usermode DLL injector for VALORANT utilizing the `SetWindowHookEx` API. This implementation operates entirely in usermode without requiring kernel drivers or manual mapping techniques.

---

## Technical Overview

The SetWindowHookEx injection method remains functional despite widespread claims to the contrary. Many commercially available VALORANT cheats (P2C) are based on this technique, often repackaged with minimal modifications and falsely marketed as proprietary, detection-proof solutions.

Common assertions that this method is "patched" or "detected" are typically misattributed. Detection events are more frequently caused by:
- DLLs signed with blacklisted or reused code signing certificates
- Signature-based detection of known cheat binaries
- Behavioral analysis of the injected payload itself

The injection vector itself remains viable.

---

## Key Improvements

- **Updated Window Class Detection** – Modified to target `VALORANTUnrealWindow`, addressing a breaking change introduced in recent game updates
- **Automatic Export Resolution** – Removes the requirement to manually specify export function names
- **Codebase Restructuring** – Improved organization and readability for maintainability
- **Stability Enhancements** – Minor internal refinements for consistent operation

---

## References

- Original Repository: [DrNseven/hookloader](https://github.com/DrNseven/hookloader)  
- Technical Discussion: [UnknownCheats Thread](https://www.unknowncheats.me/forum/valorant/702198-hookloader-fork.html)

---

## Disclaimer

This repository is provided strictly for **educational and research purposes**.  
The code is intended to demonstrate Windows API injection techniques in a controlled environment. Usage that violates software terms of service or applicable laws is neither endorsed nor supported.

---
