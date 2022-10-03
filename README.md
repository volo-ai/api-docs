# Fork of Slate API docs

## Build

```
docker run --rm --name slate -v $(pwd)/build:/srv/slate/build -v $(pwd)/source:/srv/slate/source slatedocs/slate build
```

After this command completes, you should see the built artifacts for your site in the $(pwd)/build directory, which you can then statically serve for your website.

## Run

If you wish to run the development server for Slate to aid in working on the site, run:

```
docker run --rm --name slate -p 4567:4567 -v $(pwd)/source:/srv/slate/source slatedocs/slate serve
```

and you will be able to access your site at http://localhost:4567 until you stop the running container process.
