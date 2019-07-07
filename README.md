# Timmo Bot

![Project Stage][project-stage-shield]
![Project Maintenance][maintenance-shield]
[![GitHub Activity][commits-shield]][commits]
[![License][license-shield]](LICENSE.md)

## About

Timmo Bot is a bot that helps the project by
doing all kind of administrative tasks on our PR' and issues.

This app was created using [Probot][probot].

## Installation

- Create your own GitHub app: [instructions][instructions]
- On your local machine, copy `.env.example` to `.env`.
- Go to [smee.io][smee] and click **Start a new channel**. Set `WEBHOOK_PROXY_URL` in `.env` to the URL that you are redirected to.
- [Create a new GitHub App][github-app] with:
  - **Webhook URL**: Use your `WEBHOOK_PROXY_URL` from the previous step.
  - **Webhook Secret**: `development`.
  - **Permissions & events**
    - Commit statuses **(read & write)**
    - Pull Requests **(read only)**
    - Subscribe to events **Pull request**
- Download the private key and move it to your project's directory. It will get picked up by Probot automatically.
- Edit `.env` and set `APP_ID` to the ID of the app you just created. The App ID can be found in your app settings page here
- Run `$ npm run dev`

See [Probot Deployment][deployment] documentation if you would like to run your own instance of this app.

## Contributing

This is an active open-source project. We are always open to people who want to
use the code or contribute to it.

We have set up a separate document containing our
[contribution guidelines](.github/CONTRIBUTING.md).

Thank you for being involved! :heart_eyes:

## Authors & contributors

The original setup of this repository is by [Timmo][timmo].

For a full list of all authors and contributors,
check [the contributor's page][contributors].

## License

MIT License

Copyright (c) 2018 Timmo

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

[commits-shield]: https://img.shields.io/github/commit-activity/y/timmo001/timmo-bot.svg
[commits]: https://github.com/timmo001/timmo-bot/commits/master
[contributors]: https://github.com/timmo001/timmo-bot/graphs/contributors
[timmo]: https://github.com/timmo001
[issue]: https://github.com/timmo001/timmo-bot/issues
[keepchangelog]: http://keepachangelog.com/en/1.0.0/
[license-shield]: https://img.shields.io/github/license/timmo001/timmo-bot.svg
[maintenance-shield]: https://img.shields.io/maintenance/yes/2019.svg
[project-stage-shield]: https://img.shields.io/badge/project%20stage-production%20ready-brightgreen.svg
[instructions]: https://probot.github.io/docs/development/#configure-a-github-app
[smee]: https://smee.io
[github-app]: https://github.com/settings/apps/new
[deployment]: https://probot.github.io/docs/deployment/
[probot]: https://github.com/probot/probot
