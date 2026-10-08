# NexusEco AI

NexusEco is a private AI chat app that runs a small language model directly in
the browser. I built it to explore whether useful everyday AI can rely less on
remote data-center inference.

## What it does

- Runs Qwen2.5 3B locally through WebGPU
- Saves the downloaded model in the browser for later visits
- Streams responses and keeps chat history on the device
- Renders Markdown, code blocks, and LaTeX
- Includes local file attachments and a deeper reasoning mode
- Shows clearly labeled environmental estimates
- Works in light and dark mode

Local AI is not impact-free. Device electricity and hardware still matter, and
the impact figures shown by the app are estimates.

## Try it locally

Opening the file directly will not work because browser modules require a local
web server. In this folder, run:

```bash
python -m http.server 8080
```

Then visit `http://localhost:8080` in a recent desktop version of Chrome or
Edge. The first model download is about 1.75 GB. Later visits use the browser's
cached copy unless site data has been cleared or removed by the browser.

## Publish with GitHub Pages

1. Create a public GitHub repository.
2. Upload `index.html`, `README.md`, and the `.github` folder to the repository
   root.
3. Open **Settings → Pages**.
4. Set **Source** to **GitHub Actions**.
5. Open the **Actions** tab and wait for the deployment to finish.

If GitHub's uploader does not create the hidden workflow folder, choose
**Add file → Create new file**, enter
`.github/workflows/deploy-pages.yml`, and paste in the workflow file.

## Files

- `index.html` contains the complete interface, styling, and browser runtime.
- `README.md` documents the project.
- `.github/workflows/deploy-pages.yml` publishes the site.

No backend, API key, Python service, or build command is required.
