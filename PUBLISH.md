# Publish the Lumi link site (one time)

Run these two commands in Terminal from this folder. They create the public repo
xavierpuchert.github.io and turn on GitHub Pages. Invite links then open the app:
https://xavierpuchert.github.io/friend/LUMI-XXXXXX

    cd ~/lumi/link-site && git init -q && git add -A && git commit -q -m "Lumi link site" && gh repo create xavierpuchert/xavierpuchert.github.io --public --source=. --push -d "Lumi app links"

    gh api repos/xavierpuchert/xavierpuchert.github.io/pages -X POST -f 'source[branch]=main' -f 'source[path]=/'

Later, for link.get-lumi.com: add a CNAME record "link" pointing to xavierpuchert.github.io
in Shopify (Settings, Domains, get-lumi.com, DNS settings), then set the custom domain on
the repo's Pages settings and change TapRouter.inviteHost in the app.
