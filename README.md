# Stub Extractors

Ideally datasets should extract well-formatted metadata, for example using the
[oscem-extractor-life](https://github.com/osc-em/oscem-extractor-life) or the
[oscem-extractor-materials](https://github.com/osc-em/oscem-extractor-materials).

In contrast, this repository contains dummy extractors and schemas that allow you to
work with the [SciCat Web Ingestor](https://github.com/SwissOpenEM/Ingestor) even
without rigorous metadata schemas.

This repository can be considered an incubator. Any scripts successful enough to grow to
more than a page of code should probably be migrated to their own repository.

## Extractor spec

An extractor is any executable that:

- Saves JSON to a file
- Reports progress over stdout
- Reports errors to stderr

By convention, they should support `-i` for the input directory and `-o` for the output
file. (Other conventions require extra configuration in the ingestor.) Output is
forwarded to the user; messages like `Progress: 100%` are appreciated. (No stub
extractors should require significant time to run.)

## Extractors

- `empty_extractor`: Returns and empty object

## Schemas

- `object.schema.json`: Matches any JSON object
