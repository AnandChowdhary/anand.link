# 🔗 Anand.LINK

This repository automates a multi-domain URL shortener across all my sites. Currently running on:

- https://anand.link
- https://go.a11y.co
- https://redir.oswaldlabs.com
- https://sale.melangebox.com
- https://go.o15y.com

This repository is a fork of [paramt/go.param.me](https://github.com/paramt/go.param.me) and contains only data changes. If you want to star this project or submit a pull request, do it there instead.

All the redirect URLs are maintained in a single [CSV file](redirects.csv), which is fetched by the client-side [JavaScript](script.js) each time someone visits the site. There is no dynamic content as everything is done by the client-side. 

## 💡 Usage

Redirects can be added, removed, or modified by updating [redirects.csv](redirects.csv). However, GitHub Actions makes it possible to automate this process. Creating a new issue triggers [this worksflow](.github.workflow.yml) which runs [this Python script](add_url.py). The script is set up to automatically update redirects.csv based on the issue body. 

### Add URL

In order to add a redirect, the issue must be created by me, be titled "Add URL", and have the <kbd>update redirects</kbd> label. The issue body needs to be: 

```
Short URL --> Long URL
```

### Remove URL

In order to remove a redirect, the issue must be created by me, be titled "Remove URL", and have the <kbd>update redirects</kbd> label. The issue body should contain the short URL to remove.

## 📄 License

- [MIT](./LICENSE) © [Anand Chowdhary](https://anandchowdhary.com)
- Original repo: [paramt/go.param.me](https://github.com/paramt/go.param.me)
