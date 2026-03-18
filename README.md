# Portfolio Site

This repository contains a static website ready to deploy with GitHub Pages.

## Deploy to GitHub Pages

1. Create a new GitHub repository.
2. Add the GitHub remote:

```bash
git remote add origin <your-repo-url>
```

3. Commit and push:

```bash
git add .
git commit -m "Initial site import"
git branch -M main
git push -u origin main
```

4. In GitHub, open `Settings -> Pages`.
5. Set:
   - Source: `Deploy from a branch`
   - Branch: `main`
   - Folder: `/ (root)`

## Custom Domain

After GitHub Pages is working, add your domain in `Settings -> Pages -> Custom domain`.

If you want the domain stored in the repo, add a `CNAME` file at the repository root containing only your domain name, for example:

```text
www.example.com
```

Then update DNS with your registrar:

- For apex/root domain (`example.com`): point `A` records to GitHub Pages IPs.
- For subdomain (`www.example.com`): create a `CNAME` record pointing to `<your-github-username>.github.io`.
