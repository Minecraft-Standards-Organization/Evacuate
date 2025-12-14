> [!CAUTION]
> NOT INTENDED FOR PUBLIC READING. MAY BE CHANGED INTERNALLY WITHOUT UPDATING THIS.
# 📘 Evacuate Mod Versioning Guidelines

## 🎯 Purpose
These guidelines define how *Evacuate!* versions are numbered and released, ensuring consistency, clarity, and compatibility across Forge and NeoForge builds. They follow **Semantic Versioning (SemVer)** principles.

---

## 🔢 Version Format
```
MAJOR.MINOR.PATCH-PRERELEASE][+BUILD]
```

- **MAJOR** → Breaking changes, rewrites, or incompatible updates.  
- **MINOR** → New features, additions, or significant improvements (backwards‑compatible).  
- **PATCH** → Bug fixes, small tweaks, or minor adjustments.  
- **PRERELEASE** → Optional tag for alpha, beta, or test builds.  
- **BUILD** → Optional metadata (e.g., commit hash, build ID).

---

## 🏷️ Release Types

### ✅ Stable Releases
- Format: `X.Y.Z`  
- Example: `1.7.0`  
- Used for official CurseForge/GitHub releases.  
- Always documented in the changelog and reflected in `update.json`.

---

### 🧪 Test Builds
- Format: `X.Y.Z-test.N`  
- Example: `1.7.0-test.1`  
- Internal builds for quick validation.  
- Not uploaded to CurseForge; may be shared privately.  
- Should never be marked as “release” in distribution platforms.

---

### 🟡 Alpha Releases
- Format: `X.Y.Z-alpha.N`  
- Example: `1.7.0-alpha.2`  
- Early builds with incomplete features.  
- May be unstable; intended for testers.  
- Not recommended for modpacks.

---

### 🔵 Beta Releases
- Format: `X.Y.Z-beta.N`  
- Example: `1.7.0-beta.1`  
- Feature‑complete but may contain bugs.  
- Shared for community feedback before stable release.  
- Can be uploaded to CurseForge/GitHub but clearly labeled as **Beta**.

---

## 📈 Versioning Rules
- **Increment MAJOR** when:  
  - Minecraft version compatibility changes (e.g., 1.20 → 1.21).  
  - Core systems are rewritten.  
  - Backwards compatibility is broken.
  - Updates with many new features.  

- **Increment MINOR** when:  
  - New ISO/IMO sign classes are added.  
  - New crafting recipes or mechanics are introduced.  
  - Translations or UI improvements are added.  

- **Increment PATCH** when:  
  - Bug fixes (e.g., duplicate recipe fix).  
  - Minor balance tweaks.  
  - Small visual or text corrections.  

---

## 🔗 Update.json Integration
- Stable releases (`X.Y.Z`) must update the `promos` section.  
- Pre‑releases (`alpha`, `beta`, `test`) **must not** be listed in promos.  
- Example `promos` entry:
```json
"promos": {
  "1.20.1-latest": "1.7.0",
  "1.20.1-recommended": "1.7.0"
}
