<p align="center">
  <img src="https://www.seven.io/wp-content/uploads/Logo.svg" width="250" alt="seven logo" />
</p>

<h1 align="center">seven SMS for Checkmk</h1>

<p align="center">
  Notification plugin for <a href="https://checkmk.com/">Checkmk</a> that sends SMS alerts via the seven gateway.
</p>

<p align="center">
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-teal.svg" alt="MIT License" /></a>
  <img src="https://img.shields.io/badge/Checkmk-2.x-blue" alt="Checkmk 2.x" />
  <img src="https://img.shields.io/badge/Python-3-yellow" alt="Python 3" />
</p>

---

## Features

- **Native Checkmk Notification Plugin** - Lives next to the bundled email and SMS plugins
- **Env-Var or Param-Based Auth** - Pass the API key as the first parameter or via `SEVEN_API_KEY`

## Prerequisites

- A [Checkmk](https://checkmk.com/) site
- A [seven account](https://www.seven.io/) with API key ([How to get your API key](https://help.seven.io/en/developer/where-do-i-find-my-api-key))

## Installation

```bash
git clone https://github.com/seven-io/checkmk
cd checkmk
mv seven.py /<omd-path>/sites/<sitename>/local/share/check_mk/notifications/seven
chmod +x /<omd-path>/sites/<sitename>/local/share/check_mk/notifications/seven
```

Replace `<omd-path>` (typically `/omd`) and `<sitename>` with your Checkmk paths.

## Configuration

In Checkmk, go to **Setup > Notifications** and add a new rule. Pick *seven* as the notification method and provide the seven API key in one of two ways:

- **Plugin parameter** - Pass the API key as the first parameter to the plugin in the notification rule
- **Environment variable** - Set `SEVEN_API_KEY` in the site's profile

## Support

Need help? Feel free to [contact us](https://www.seven.io/en/company/contact/) or [open an issue](https://github.com/seven-io/checkmk/issues).

## License

[MIT](LICENSE)
