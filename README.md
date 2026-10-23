# Rise 15.1 SidelineHD site

SidelineHD team: https://sidelinehd.com/rise-15-1
Team ID: `xyJr-TmSh01-ris-EGHORMSTMvVS`

## GitHub setup

1. Create a **new public repository** named `rise-15-1-volleyball` (do not initialize it with README).
2. Upload all contents of this ZIP **to the repository root**, including `index.html`, `collect.py`, `config.json`, and the `data/` folder.
3. GitHub's web upload sometimes omits `.github` hidden folders. If so, create `.github/workflows/update-clips.yml` manually and paste the supplied workflow file.
4. In **Settings → Actions → General → Workflow permissions**, select **Read and write permissions**.
5. Under **Actions**, run **Update SidelineHD clip data** manually once.
6. In **Settings → Pages**, choose **Deploy from a branch**, branch `main`, folder `/ (root)`.
7. Website URL should be `https://wvuraw.github.io/rise-15-1-volleyball/` if you create the repository with the suggested name under `wvuraw`.

The website has empty JSON placeholders so it loads before the first workflow run. The collector retrieves the team roster and games, then clips for any claimed players. Unclaimed players still appear on the roster. If there are no games or clips yet, the site shows an empty-state message. New data is scheduled every three hours, though GitHub may delay scheduled jobs.

These are undocumented SidelineHD endpoints; they can change. Clip tags are not independently verified stats. No team PINs or authorization tokens are needed.
