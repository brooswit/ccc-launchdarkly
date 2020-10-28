# LaunchDarkly SDK for ComputerCraft (A MineCraft mod)

[![Circle CI](https://circleci.com/gh/brooswit/ld-computercraft-client-sdk/tree/master.svg?style=svg)](https://circleci.com/gh/brooswit/ld-computercraft-client-sdk/tree/master)

## LaunchDarkly overview

[LaunchDarkly](https://www.launchdarkly.com) is a feature management platform that serves over 100 billion feature flags daily to help teams build better software, faster. [Get started](https://docs.launchdarkly.com/docs/getting-started) using LaunchDarkly today!

[![Twitter Follow](https://img.shields.io/twitter/follow/launchdarkly.svg?style=social&label=Follow&maxAge=2592000)](https://twitter.com/intent/follow?screen_name=launchdarkly)

## Reminder: this is not a supported SDK

This SDK is provided as-is and is not supported in any capacity by LaunchDarkly. [Click here to see all SDKs that are officially supported by LaunchDarkly](https://docs.launchdarkly.com/sdk#available-sdks)

## Getting started

The ComputerCraft SDK requires that JSON and Base64 libraries are already installed.

The `LDClient` script can be downloaded using the following:

```
local w = fs.open("LDClient", "w")
local r = http.get("https://raw.githubusercontent.com/brooswit/ld-computercraft-client-sdk/main/LDClient.lua")
w.write(r.readAll())
w.close()
```

Once installed, you can initialize and use the SDK. Here is a short example:

```
os.loadAPI("LDClient")
local ldClient = LDClient("YOUR-CLIENTSIDE-ID")
print(ldClient.variation("YOUR-FLAG-KEY"))
```

## Learn more

Check out our [documentation](https://docs.launchdarkly.com) for in-depth instructions on configuring and using LaunchDarkly.

## Testing

TODO

## Contributing

We encourage pull requests and other contributions from the community. Check out our [contributing guidelines](CONTRIBUTING.md) for instructions on how to contribute to this SDK.

## About LaunchDarkly

* LaunchDarkly is a continuous delivery platform that provides feature flags as a service and allows developers to iterate quickly and safely. We allow you to easily flag your features and manage them from the LaunchDarkly dashboard.  With LaunchDarkly, you can:
    * Roll out a new feature to a subset of your users (like a group of users who opt-in to a beta tester group), gathering feedback and bug reports from real-world use cases.
    * Gradually roll out a feature to an increasing percentage of users, and track the effect that the feature has on key metrics (for instance, how likely is a user to complete a purchase if they have feature A versus feature B?).
    * Turn off a feature that you realize is causing performance problems in production, without needing to re-deploy, or even restart the application with a changed configuration file.
    * Grant access to certain features based on user attributes, like payment plan (eg: users on the ‘gold’ plan get access to more features than users in the ‘silver’ plan). Disable parts of your application to facilitate maintenance, without taking everything offline.
* LaunchDarkly provides feature flag SDKs for a wide variety of languages and technologies. Check out [our documentation](https://docs.launchdarkly.com/docs) for a complete list.
* Explore LaunchDarkly
    * [launchdarkly.com](https://www.launchdarkly.com/ "LaunchDarkly Main Website") for more information
    * [docs.launchdarkly.com](https://docs.launchdarkly.com/  "LaunchDarkly Documentation") for our documentation and SDK reference guides
    * [apidocs.launchdarkly.com](https://apidocs.launchdarkly.com/  "LaunchDarkly API Documentation") for our API documentation
    * [blog.launchdarkly.com](https://blog.launchdarkly.com/  "LaunchDarkly Blog Documentation") for the latest product updates
    * [Feature Flagging Guide](https://github.com/launchdarkly/featureflags/  "Feature Flagging Guide") for best practices and strategies
