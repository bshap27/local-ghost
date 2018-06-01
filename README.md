## What's Up
This repo allows you to quickly spin up a local version of Ghost for quick theme development.

## Getting Started
1. Get Docker on your local machine, https://docs.docker.com/install/
2. Clone this repo and run `docker-compose up`
3. Navigate to the local ghost instance at `http://localhost:3000/`
to make sure its up and running and setup the admin by navigating to `http://localhost:3000/ghost/`
4. Test working on a new theme i.e. not casper by cloning the Attila theme into
your src folder, making changes to it, and running the gulp task `gulp watch`.
  a. `cd src`
  b. `rm .gitkeep`
  c. `git clone https://github.com/zutrinken/attila.git .`
  d. `gulp watch` to copy your custom theme code into `content/themes/custom-theme`
  e. In `src/index.hbs` add `<h2>BOOM</h2>` or whatever you want above the header tag
  f. `docker restart ghost-theme-dev` to make the change showup (TODO - figure out how to make docker pickup these changes without restart)
  g. Go to ghost admin, click on design, and under themes "activate" the Attila theme
  h. Navigate back to the ghost homepage and you should see BOOM at the top of the page

