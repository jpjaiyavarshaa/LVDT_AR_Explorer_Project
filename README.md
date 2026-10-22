# LVDT Explorer — 3D + AR Educational Website

A responsive educational microsite about the Linear Variable Differential Transformer (LVDT), with:
- step-by-step working principle
- interactive displacement/output simulator
- illustrative 3D GLB model
- AR button using `<model-viewer>` (supported phones/browsers only)
- quick quiz

## Publish on GitHub Pages
1. Sign in to GitHub and create a **public** repository, e.g. `lvdt-ar-explorer`.
2. Upload `index.html`, the `assets` folder, and this README. Keep `assets/lvdt.glb` in that exact location.
3. Open the repository **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Choose branch `main` and folder `/(root)`, then Save.
6. Wait for GitHub Pages to publish. Your URL will look like `https://YOUR-USERNAME.github.io/lvdt-ar-explorer/`.
7. Open the URL on a phone and test the 3D model. AR depends on device/browser support; iPhone/iPad may use Quick Look and many Android phones use Scene Viewer/WebXR.

## Make a QR code after publishing
The QR must encode your actual live URL. Replace `YOUR-USERNAME` below with your GitHub username and run this command in a terminal if Python and `qrcode` are installed:

```bash
python -m pip install "qrcode[pil]"
python -c "import qrcode; qrcode.make('https://YOUR-USERNAME.github.io/lvdt-ar-explorer/').save('lvdt-qr.png')"
```

Alternatively, open a reputable QR-code generator, paste the live URL, generate the code, and download it. Scan-test the printed code before putting it on a poster.

## Notes
- The simulator uses illustrative values (5 V at null and a linear 0.35 V/mm change per secondary) to explain the concept; these are not real sensor specifications.
- The 3D model is a simplified educational visual, not a manufacturing drawing.
- For a real classroom demo, verify the model and AR behaviour on the target phones and campus Wi-Fi before presenting.
