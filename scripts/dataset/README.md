# Dataset release

Export the versions dataset into a ZIP file and publish it to GitHub releases.

## Configuring

You can change the configuration in the appropriate config file in the `config` folder.

```json
{
  "dataset": {
    "servicesRepositoryName": "Name of the services declarations repository",
    "versionsRepositoryURL": "GitHub repository where the dataset will be published as a release; recommended to be the versions repository for discoverability and tagging purposes"
  }
}
```

## Running

To export the dataset into a local ZIP file:

```sh
node scripts/dataset/main.js [$filename]
```

To export the dataset into a ZIP file and publish it on GitHub releases:

```sh
node scripts/dataset/main.js --publish
```

To export, publish the dataset and remove the local copy that was created after it has been uploaded:

```sh
node scripts/dataset/main.js --publish --remove-local-copy
```

To schedule export, publishing and local copy removal:

```sh
node scripts/dataset/main.js --schedule --publish --remove-local-copy
```

## Adding renaming rules

See the [renamer module documentation](../renamer/README.md).