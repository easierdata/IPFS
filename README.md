# IPFS Extension Specification

- **Title:** IPFS
- **Identifier:** <https://github.com/easierdata/IPFS/blob/main/json-schema/schema.json>
- **Field Name Prefix:** IPFS 
- **Scope:** Item, Asset
- **Extension [Maturity Classification](https://github.com/radiantearth/stac-spec/tree/master/extensions/README.md#extension-maturity):** Proposal
- **Owner**: @TaylorOshan @leonardzh @jsolly 

This document explains the IPFS Extension to the [SpatioTemporal Asset Catalog](https://github.com/radiantearth/stac-spec) (STAC) specification.
This extension adds fields to STAC Item and Asset objects, allowing for details related to IPFS storage access associated with a STAC Item.

- Examples:
  - [Item example](examples/item.json): Shows the basic usage of the extension in a STAC Item
  - [Item example](examples/item2.json): Another example of basic usage.
- [JSON Schema](json-schema/schema.json)
- [Changelog](./CHANGELOG.md)

## Item Fields

| Field Name           | Type                      | Description |
| -------------------- | ------------------------- | ----------- |
| ipfs:payload-cid         | string | Each item is associated with a single content ID hash |

## Asset Fields
| Field Name           | Type                      | Description |
| -------------------- | ------------------------- | ----------- |
| ipfs:cid   | string                    | Each asset is associated with a single content ID hash |

## Contributing

All contributions are subject to the
[STAC Specification Code of Conduct](https://github.com/radiantearth/stac-spec/blob/master/CODE_OF_CONDUCT.md).
For contributions, please follow the
[STAC specification contributing guide](https://github.com/radiantearth/stac-spec/blob/master/CONTRIBUTING.md) Instructions
for running tests are copied here for convenience.

### Running tests

The same checks that run as checks on PR's are part of the repository and can be run locally to verify that changes are valid. 
To run tests locally, you'll need `npm`, which is a standard part of any [node.js installation](https://nodejs.org/en/download/).

First you'll need to install everything with npm once. Just navigate to the root of this repository and on 
your command line run:
```bash
npm install
```

Then to check markdown formatting and test the examples against the JSON schema, you can run:
```bash
npm test
```

This will spit out the same texts that you see online, and you can then go and fix your markdown or examples.

If the tests reveal formatting problems with the examples, you can fix them with:
```bash
npm run format-examples
```
