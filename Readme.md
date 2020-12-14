# Lando VIP Boilerplate

This tool will download and set up a fresh copy of wordpress and the VIP site of your choice

## Usage

```bash
git clone git@github.com:yikesinc/lando-vip-boilerplate.git site-name
cd site-name && code . # Opens directory in VS Code, change to match your editor
```
Open the `.lando.yml` file and edit the `name` property. Make sure the name is the same as the repo of the vip site.

For example, if the repo is `wpvipcom/site-name`, the name property should say `site-name`

Then go back to the terminal and execute the setup script:
```bash
./start
```

## Requirements

- **Lando**

### Mac
```bash
brew cask install lando
```

### Windows
[Visit this page](https://docs.lando.dev/basics/installation.html#windows)

## What does it do?
- Asks you to authenticate your ssh-key
- Asks if the site is a multisite
- Downloads WordPress
- Downloads the VIP client's website files
- Starts the docker server
- Sets up the `wp-config.php` file
- Runs `wp core install` or `wp core multisite-install`
- Downloads the VIP Go mu-plugins
- Cleans up, leaving NO TRACE OF ITS EXISTENCE

Whatever you put as the name property in the `.lando.yml` file will be both username and password
