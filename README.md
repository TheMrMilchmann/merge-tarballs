# merge-tarballs

A GitHub Action to merge tarballs.


## Usage

```yaml
steps:
  - id: bundle
    uses: TheMrMilchmann/merge-tarballs@v1
    with:
      glob: artifacts/**
      archive: ./bundle.tgz
      
outputs:
  archive: ${{ steps.bundle.outputs.archive }}
```

### Inputs

| Input         | Description                                      | Default |
|---------------|--------------------------------------------------|---------|
| `archive`     | The path to write the merged archive to.         |         |
| `glob`        | A glob pattern matching the tarballs to merge.   |         |
| `compression` | The compression method for the (merged) archive. | `"gz"`  |


### Outputs

| Output    | Description                     |
|-----------|---------------------------------|
| `archive` | The path to the merged archive. |


## Versioning

This action is strictly following [SemVer 2.0.0](https://semver.org/spec/v2.0.0.html).
Thus, it is recommended to pin the action against specific MAJOR version. This
can be achieved by using the `v${MAJOR}` branch.

To get an overview about the action's versions, see the [changelog](docs/changelog/README.md).


## License

```
MIT License

Copyright (c) 2025-2026 Leon Linhart

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
```
