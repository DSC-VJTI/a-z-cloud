# A-Z Cloud

<img src=".github/assets/a-z-cloud-hero.png" alt="A-Z Cloud: Learn the A-Z of cloud in 26 days!" height=33% width=33% />

An initiative by the Cloud Computing Core Team at [GDSC VJTI](https://gdscvjti.tech)

## Running the website locally

### Prerequisites

- Go version 1.14 or higher. Install Go from [go.dev/doc/install](https://go.dev/doc/install)

- The latest Hugo version. Install Hugo from [gohugo.io](https://gohugo.io/getting-started/installing/). Verify your installation with
  ```
  hugo version | grep extended
  ```
  The extended build is required for PostCSS and SCSS to work with this template.

### Installation

1. Clone the repository along with the Docsy theme submodule

   ```bash
   git clone --recurse-submodules --depth 1 https://github.com/DSC-VJTI/a-z-cloud.git
   ```

2. Install the required `node_modules` for SCSS and PostCSS to work

   ```bash
   cd a-z-cloud
   npm install
   ```

3. Build and run the webiste locally

   ```
   hugo server
   ```

   The webiste will now be available on `localhost:1313/a-z-cloud/`

4. To verify whether your local build will be succesfully deployed, run
   ```
   hugo -D
   ```
   If no errors are encountered, this generates a `public` directory

### Running a container locally

You can run `a-z-cloud` inside a [Docker](https://docs.docker.com/)
container, the container runs with a volume bound to the `a-z-cloud`
folder. This approach doesn't require you to install any dependencies other
than [Docker Desktop](https://www.docker.com/products/docker-desktop) on
Windows and Mac, and [Docker Compose](https://docs.docker.com/compose/install/)
on Linux.

1. Build the docker image

   ```bash
   docker-compose build
   ```

1. Run the built image

   ```bash
   docker-compose up
   ```

   > NOTE: You can run both commands at once with `docker-compose up --build`.

1. Verify that the service is working.

   Open your web browser and type `http://localhost:1313` in your navigation bar,
   This opens a local instance of the docsy-example homepage. You can now make
   changes to the docsy example and those changes will immediately show up in your
   browser after you save.

### Cleanup

To stop Docker Compose, on your terminal window, press **Ctrl + C**.

To remove the produced images run:

```console
docker-compose rm
```

For more information see the [Docker Compose
documentation](https://docs.docker.com/compose/gettingstarted/).

## Troubleshooting

As you run the website locally, you may run into the following error:

```
➜ hugo server

INFO 2021/01/21 21:07:55 Using config file:
Building sites … INFO 2021/01/21 21:07:55 syncing static files to /
Built in 288 ms
Error: Error building site: TOCSS: failed to transform "scss/main.scss" (text/x-scss): resource "scss/scss/main.scss_9fadf33d895a46083cdd64396b57ef68" not found in file cache
```

This error occurs if you have not installed the extended version of Hugo.
See our [user guide](https://www.docsy.dev/docs/getting-started/) for instructions on how to install Hugo.

[alternate dashboard]: https://app.netlify.com/sites/goldydocs/deploys
[deploys]: https://app.netlify.com/sites/docsy-example/deploys
[docsy user guide]: https://docsy.dev/docs
[docsy]: https://github.com/google/docsy
[example.docsy.dev]: https://example.docsy.dev
[hugo theme]: https://www.mikedane.com/static-site-generators/hugo/installing-using-themes/
[netlify]: https://netlify.com
