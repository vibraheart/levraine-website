# Deploy LEVRAINE to Cloudflare Pages

## Architecture

- **Namecheap**: domain registrar for `levraine.com`
- **GitHub**: source code repository
- **Cloudflare Pages**: free static hosting, HTTPS, and automatic deploys

## 1. Create the GitHub repository

1. Sign in to GitHub.
2. Create a new repository, for example `levraine-website`.
3. Keep it **Private** if you do not want the website source publicly browsable.
4. Upload all files from this repository to the repository root.
5. Commit the files.

Do not put passwords, API keys, Amazon credentials, or Namecheap credentials into the repository.

## 2. Create a Cloudflare Pages project

1. Sign in to Cloudflare.
2. Go to **Workers & Pages**.
3. Choose **Create application** → **Pages** → **Connect to Git**.
4. Connect GitHub and select the `levraine-website` repository.
5. Deployment settings:
   - Framework preset: `None`
   - Build command: leave blank
   - Build output directory: `/`
6. Deploy.

Cloudflare will first provide a temporary `*.pages.dev` address. Open it and verify the website before connecting the real domain.

## 3. Add levraine.com to Cloudflare

In Cloudflare, add `levraine.com` as a site/domain and follow the nameserver instructions Cloudflare displays for your account.

## 4. Change nameservers at Namecheap

In Namecheap:

1. Go to **Domain List**.
2. Choose **Manage** beside `levraine.com`.
3. Find **Nameservers**.
4. Choose **Custom DNS**.
5. Enter the two Cloudflare nameservers shown in your Cloudflare account.
6. Save.

Use only the nameservers Cloudflare gives you. Do not copy nameservers from examples online.

DNS propagation can take some time. Cloudflare will show when the domain becomes active.

## 5. Connect the custom domain to Pages

In the Cloudflare Pages project:

1. Open **Custom domains**.
2. Add `levraine.com`.
3. Also add `www.levraine.com` if you want the `www` version.
4. Make `levraine.com` the canonical domain.

Cloudflare will provision HTTPS automatically.

## 6. Final checks before the Amazon Ads API application

Open `https://levraine.com` and confirm:

- HTTPS works with no certificate warning.
- `Marship Vibraheart Inc.` is visible on the site.
- LEVRAINE is clearly presented as the brand.
- The company is described as a Canadian e-commerce company.
- Internal advertising/analytics technology is described as being for the company's own operations.
- The contact email is real and working.
- No placeholder text remains.
- Only images you have rights to use are displayed.
- `https://levraine.com/privacy.html` works.

## Updating the website later

After Cloudflare Pages is connected to GitHub, every push to the production branch will automatically redeploy the site. You do not need to upload files to Namecheap.
