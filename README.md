# Unified Module iOS Builder

Build iOS for Unified Module.

## Example Usage

```yml
steps:
  - label: Build iOS
    plugins:
        - ssh://git@github.com/thanyalukj/um-ios-builder-buildkite-plugin.git#v1.0.0:
            platform: 'ios-contract'
            file_path: 'AmplitudeUMContract.podspec'
    agents:
      queue: build
```

## Configuration

### `platform` (Required, string)

Specifies platform. Accepted values are: `ios-contract` and `ios-library`

### `file_path` (Required, string)

Specifies the file_path where the plugin is looking for the version. For example: `AmplitudeUM.podspec` or `AmplitudeUMContract.podspec`

## Development

To execute the tests, run the following command:

```shell
docker-compose run --rm tests
```
