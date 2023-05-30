# Example of mirroring from r-universe

Example github action workflow to mirror the cranlike-repository from https://jeroen.r-universe.dev to GitHub pages using the r-universe snapshot api.

To copy this workflow follow these 3 steps:

 - Copy the workflow file from [.github/workflows/mirror.yml](.github/workflows/mirror.yml)
 - In your GitHub repository settings, enable GitHub pages on the `main` branch
 - In your GitHub repository settings, under "actions > general" set "Workflow permissions" to "read and write" such that the action can push back to this repository.

Now you can manually trigger the workflow under your actions tab.

Once the action has completed, R can install directly from the backup, for example:

```r
install.packages("curl", repos = 'https://jeroen.github.io/backup')
```
