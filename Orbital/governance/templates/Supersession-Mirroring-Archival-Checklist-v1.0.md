# **Generic Template: 10‑Action Supersession, Mirroring & Archival Checklist (v1.0)**

---

## **1. Confirm Artifact Scope**  
Identify all repositories containing the prior version of the artifact.  
Verify that each repo requires both archival of the old version and mirroring of the new version.

---

## **2. Ensure Archive Directory Exists**  
Confirm or create the standardized archival path:

```
<Repo>/Orbital/governance/<category>/archive/
```

This directory must exist before moving the prior version.

---

## **3. Move Prior Version to Archive**  
Relocate the previous version (e.g., vX.X) into the archive directory.  
Do not modify its content beyond adding the provenance footer.

---

## **4. Apply Superseded Footer**  
Append the standardized superseded provenance footer:

```
Provenance — Superseded
This version is superseded by <new-version> and retained only for provenance and audit continuity.
```

---

## **5. Place New Version in Active Path**  
Copy the new authoritative version into the active governance path:

```
<Repo>/Orbital/governance/<category>/<ArtifactName>-<new-version>.md
```

---

## **6. Apply Active Footer**  
Append the standardized active provenance footer:

```
Provenance — Active
This is the current and authoritative version. It supersedes all earlier versions.
```

---

## **7. Verify Lineage Stability**  
Confirm that lineage references remain unchanged between versions.  
Lineage must not be altered during supersession.

---

## **8. Commit Archival Update**  
Use the uniform commit message:

```
Archive: <ArtifactName> (<old-version>)
```

This commit records the archival of the prior version.

---

## **9. Commit Mirrored New Version**  
Use the uniform mirroring commit message:

```
Mirror Update: <ArtifactName> (<new-version>)
```

This establishes the new version as authoritative across all mirrors.

---

## **10. Perform Cross‑Repo Consistency Check**  
Verify that all repositories now contain:

- archived prior version with Superseded footer  
- active new version with Active footer  
- identical file paths  
- identical commit messages  
- identical artifact content  
- correct lineage and provenance states  

This ensures governance stability and prevents supersession drift.

---

# **Summary (Generic Template)**

This template gives you:

- a **universal 10‑step workflow**  
- reusable across any directive or governance artifact  
- stable for multi‑repo operations  
- aligned with NDH‑Orbital supersession rules  
- safe for mirroring and archival cycles  


