# UTA CodePush CLI

A fork of Microsoft's CodePush CLI, customized for UpdateTheApp.com service to enable React Native over-the-air updates.

## Installation

```shell
npm install -g @updatetheapp/uta-codepush-cli
```

## Getting Started

1. Generate an API key from [UpdateTheApp Dashboard](https://updatetheapp.com/dashboard/settings/api-keys)
2. Login using your API key:

```shell
uta login --accessKey <KEY>
```

3. Verify your authentication:

```shell
uta whoami
```

4. Deploy updates to your React Native app:

```shell
uta release-react <appName> <platform> [--deploymentName <deploymentName>]
```

## Currently Supported Commands

### Authentication

- `uta login --accessKey <KEY>` - Authenticate using API key from UpdateTheApp.com
- `uta whoami` - Display current authentication status

### App Updates

- `uta release-react <appName> <platform>` - Release a React Native update
  - Options:
    - `--deploymentName <name>` - Deployment to release to (default: "Staging")
    - `--description <desc>` - Description of the changes
    - `--mandatory` - Make the update mandatory
    - `--targetBinaryVersion <version>` - Target specific binary versions

## Original Project

This is a fork of [Microsoft&#39;s CodePush CLI](https://github.com/microsoft/code-push-server), licensed under the MIT License.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
