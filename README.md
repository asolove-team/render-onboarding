# render-onboarding

This is a simple Node.js application that is used to help train new Render employees
about how users interact with our product.

The app only does a few things:
- runs an http server that returns information about the environment where it's run
- tracks a hit counter via redis, if given a connection to a redis instance

## How to run locally

1. Have a running redis instance
2. Install dependencies with `npm install`
3. Configure your environment so the `REDIS_URL` environment variable has the URL of your redis instance.
4. Start the server with `npm start`

## How to run on Render

Well, that's where the fun begins!

Imagine yourself as founder of a new and exciting tech product company. You have a local demo
of your product, but don't know anything about infrastructure. You just want your app to run,
hopefully scalably, without having to think about it much.

Your task is to finish as much as you can of the below. Try using Render's public docs if you
run into challenges, but ask the person leading this session if you get stuck and need help.

1. Fork this repo to your own account.
1. Get the Node service running on Render as quickly as possible.
   a. Put `npm install` as the build command
   b. Put `npm start` as the start command
2. Set up a Redis instance on Render and configure it to be used by the service.
3. Configure Render to automatically deploy new copies of your app whenever you make PRs to the repo
4. Make a PR that improves the page in some way (at minimum, changes to your name!). Make sure you view the Render preview of that change _before_ merging the change to production.

Extra credit choose-your-own-adventure options:
- Take the configuration you've done via the Render Dashboard and instead use Render's Infrastructure-as-Code product (Blueprints) to manage your services in your git repo.
- Configure a custom domain so your websie doesn't run on {something}.onrender.com
- Set up a background task that automatically resets (or increments) the hit counter on a schedule
- Frontend: make the sample page prettier, and submit the changes back as a PR to the original repo.
- Ambitious: separate the html content from the dynamic hit counter data, and build an API endpoint to fetch the hit counter state. Move the html content to a static site hosted by a CDN for performance.
