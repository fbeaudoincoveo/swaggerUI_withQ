#Coveo SwaggerUI Doc Testing Environment

This can be used to test the display of custom Swagger files in the SwaggerUI generated site.

##Testing With Custom JSON Swagger Files

In the `./docs.html` file, set the `TESTING_LOCALLY` variable to `true` (otherwise, the site will be generated from the
actual JSON Swagger files hosted on `https://platform.coveo.com/api-docs/`).

If you want to test from locally stored custom JSON Swagger files, you can simply overwrite the example files in the
`./api-docs-tests/` folder of your local copy of the repository.

If you would rather test from remotely stored custom JSON Swagger files or from JSON Swagger files stored under another
local path, then you can easily change the TEST_CUSTOM_PATH and/or TEST_CUSTOM_HOST to suit your needs.

In any case, the custom JSON Swagger file names have to map correctly to the original APIs. Thus, files with the
following names can very easily be tested:

- Platform.json
- Index.json
- SecurityCache.json
- Source.json
- Activity.json
- Privilege.json
- UsageAnalytics.json
- PushApi.json
- Extension.json

If you want to test other custom files, you simply have to add them manually in the `./docs.html` file:

```javascript
addApi('New API Name', PLATFORM_HOST + API_DOCS_PREFIX + 'NewApiName' + TEST_EXTENSION);
```