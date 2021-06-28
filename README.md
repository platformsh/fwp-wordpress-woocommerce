# WordPress template for Flexible Web Publisher (FWP) with Woocommerce on Platform.sh

This project provides a starter kit for WordPress projects hosted on by Flexible Web Publisher on Platform.sh. It is primarily an example, although could be used as the starting point for a real project.  It is built using Composer, via the popular <a href="https://github.com/johnpbloch/wordpress">johnpbloch/wordpress</a> script.

This template has been consciously build to allow FWP users not to worry about ssh setup to deploy their application and manage it from their Wordpress backend only.

1) Clone this repository

2) Create a new platform.sh project

```
platform project:create
```

3) Add specific environment variables

```
platform variable:create -y -p <project> -e master --level environment --name env:ADMIN_USER --value <user>
platform variable:create -y -p <project> -e master --level environment --name env:ADMIN_EMAIL --value <email>
platform variable:create -y -p <project> -e master --sensitive true --level environment --name env:ADMIN_PASSWORD --value <yourpassword>
```

4. Push to platform.sh

```
platform project:set-remote <project>
git push platform master
```
