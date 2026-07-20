# Shipsonic Biofouling Intelligence & Compliance Template

> **Statutory Framework:** IMO Resolution MEPC.378(80) / MEPC.207(62)
> **Purpose:** Rapid generation of localized, auditable Biofouling Management Plans (BFMP).

## 🚀 Getting Started

1. Click the green **"Use this template"** button at the top of this repository.
2. Select **"Create a new repository"**, pick your organization, and name your new repository (e.g., `bfmp-mv-shipsonic-vanguard`).
3. Clone your new repository and open `index.html`.

## 🛠️ Deployment Configuration

To permanently hardcode a specific vessel profile into the deployment application without using the wizard every time:
1. Open `index.html`.
2. Locate the `<script>` architecture block at the bottom of the file.
3. Modify the window listener to inject default structural parameters:

```javascript
window.addEventListener('DOMContentLoaded', () => {
    // Inject permanent vessel identity defaults
    document.getElementById('vesselName').value = "Your Vessel Name Here";
    document.getElementById('imoNumber').value = "9XXXXXX";
    document.getElementById('flagState').value = "SG";
    
    updateWizardControls();
});
