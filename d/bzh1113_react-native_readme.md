# React Native [![Build Status](https://travis-ci.org/facebook/react-native.svg?branch=master)](https://travis-ci.org/facebook/react-native) [![Circle CI](https://circleci.com/gh/facebook/react-native.svg?style=svg)](https://circleci.com/gh/facebook/react-native) [![npm version](https://badge.fury.io/js/react-native.svg)](https://badge.fury.io/js/react-native)

React Native enables you to build world-class application experiences on native platforms using a consistent developer experience based on JavaScript and [React](http://u.720life.cn/g/2b5f360ced91899e6d7809fb5ee1ea1fbd77b72146743bf5b007101f454a72b8bad7cef8ac1fbe8d5eac490b2e18164a  The focus of React Native is on developer efficiency across all the platforms you care about - learn once, write anywhere. Facebook uses React Native in multiple production apps and will continue investing in React Native.

Supported operating systems are >= Android 4.1 (API 16) and >= iOS 8.0.

- [Getting Started](#getting-started)
- [Getting Help](#getting-help)
- [Documentation](#documentation)
- [Examples](#examples)
- [Extending React Native](#extending-react-native)
- [Upgrading](#upgrading)
- [Opening Issues](#opening-issues)
- [Contributing](#contributing)
- [License](#license)

## Introduction

See the official [React Native website](http://u.720life.cn/g/2b5f360ced91899e6d7809fb5ee1ea1fbd77b72146743bf5b007101f454a72b8952c5ab6a9f67773d5fa149ce04d603c)  for an introduction to React Native.

## Getting Started

- Follow the [Getting Started guide](http://u.720life.cn/g/2b5f360ced91899e6d7809fb5ee1ea1fbd77b72146743bf5b007101f454a72b87a2bdddc06f4944f2f425154bf588abfd36f973cc651e61fb117eef71b0b4379658fb5bb1ee2e44dc0cfe203d0c45fe0)  to install React Native and its dependencies.
- Check out this [tutorial](http://u.720life.cn/g/2b5f360ced91899e6d7809fb5ee1ea1fbd77b72146743bf5b007101f454a72b84a7f7d6a2be49d213f77c430389d6b2071202e74504e128b52c091817abb0bd3f98030f9e5a607cfcbeeae9d14fe1dbe)  to walk through your first project that fetches real data and displays it in a list.
- [Open the UIExplorer example project](#examples) to see a list of components that ship with React Native.
- Install the React Developer Tools for [Chrome](http://u.720life.cn/g/011bcbff60d4bdcdf5b89348f1b4fec4ea1629e5a5711d79823204fb51bba15e5e35c30c683c012a6740f1b7adbafa5908a2dd89a62407a377169d4740baaa6c2f9d072ef5406ed5e04ace3e816e254e859a56bf7c6694a4174718b9d5031f5d)  or [Firefox](http://u.720life.cn/g/7aac0cfb1536aefff2f4add2a87f8cebc02f3bdae0d160fedaf6bbd4d1c13cbbcf4c48fdc29a07681866532fba2861eb347305ccd1e4f1b1936e5fdd190b4c3e)  for better debugging [(read more)](http://u.720life.cn/g/2b5f360ced91899e6d7809fb5ee1ea1fbd77b72146743bf5b007101f454a72b87983594087f7388d813a2497db8714ab09603da4616b1ae95970a6bbc866f9fd 
- Try out apps from the [Showcase](http://u.720life.cn/g/2b5f360ced91899e6d7809fb5ee1ea1fbd77b72146743bf5b007101f454a72b8b622a5d067c4b47762c5b03101659be429ae3147d557ca2394a344b2ef25135f)  to see what React Native is capable of!

## Getting Help

Please use these community resources for getting help. We use the GitHub issues for tracking bugs and feature requests and have limited bandwidth to address them.

- Ask a question on [StackOverflow](http://u.720life.cn/g/87bbd50441ad714fa4b3a92b06a390573fc86eb7d24a082f77a1e4ba31fd4b29)  and tag it with `react-native`
- Chat with us on [Reactiflux](http://u.720life.cn/g/f2a7d7b12e1fc16eaafd863db538a1835e40a2a4fe5c3388942951a58c44509b8e2c6145a1f95fe59b42b3aebc3895aa)  in #react-native
- Articulate your feature request or upvote existing ones on [Product Pains](http://u.720life.cn/g/27a80ee59655d78d4485b61b75d0940c16a1ae56057dc4df753df363ec9249553b729e07b6ebd048a0293f8a1ff417ba) 
- Start a thread on the [React Discussion Board](http://u.720life.cn/g/255826a2d93edb3dacc552364063ec9cfe881d7fd1d80089d8bccb1a23e212ff) 
- Join #reactnative on IRC: chat.freenode.net
- If it turns out that you may have found a bug, please [open an issue](#opening-issues)

## Documentation

[The website’s documentation](http://u.720life.cn/g/2b5f360ced91899e6d7809fb5ee1ea1fbd77b72146743bf5b007101f454a72b8a40fe9455460c9898705736ba61e6a67)  is divided into multiple sections.
- There are **Guides** that discuss topics like [debugging](http://u.720life.cn/g/2b5f360ced91899e6d7809fb5ee1ea1fbd77b72146743bf5b007101f454a72b87983594087f7388d813a2497db8714abb87d5ff9e5cb19f6a08d9a607447fc22  [integrating with existing apps](http://u.720life.cn/g/2b5f360ced91899e6d7809fb5ee1ea1fbd77b72146743bf5b007101f454a72b84bf4ac077f243416b1e0091924ed2661ab2a1fba16e4d1483d37672527077e45aea74cff3095355446e510a7b58738018e2aa3b3cda5717b987b1d3b9ffd5111  and [the gesture responder system](http://u.720life.cn/g/2b5f360ced91899e6d7809fb5ee1ea1fbd77b72146743bf5b007101f454a72b8ae25f15db79df5de8a4731b2a1f72d17f51f8ca1065f017217a1a48f7fa175dc7f5997663c93e9ee6626ed316abaeb12 
- The **Components** section covers React components such as [`View`](http://u.720life.cn/g/2b5f360ced91899e6d7809fb5ee1ea1fbd77b72146743bf5b007101f454a72b8dae2e02ad32690ec1eb809142bc91565c420bd11ca24c0e6bda9fd1d032851e9)  and [`Navigator`](http://u.720life.cn/g/2b5f360ced91899e6d7809fb5ee1ea1fbd77b72146743bf5b007101f454a72b884310e36dc45681a9589c50f45c535854004215214374fcbb6828cde3d10aefe 
- The **APIs** section covers other libraries like [Animated](http://u.720life.cn/g/2b5f360ced91899e6d7809fb5ee1ea1fbd77b72146743bf5b007101f454a72b8b396fb95f0dc0985499d8e98e87db5583d828f61c5ae59c1558897a3158c1d29)  and [StyleSheet](http://u.720life.cn/g/2b5f360ced91899e6d7809fb5ee1ea1fbd77b72146743bf5b007101f454a72b8b919724b4d2ef73f59613c73d9b80a2aefcff5adbc995e73c02c383433211770)  that aren’t React components themselves.
- Finally, React Native provides a small number of **Polyfills** that offer web-like APIs.

Another great way to learn more about the components and APIs included with React Native is to read their source. Look under the `Libraries` directory for components like `ScrollView` and `Navigator`, for example. The UIExplorer example is also here to demonstrate some of the ways to use these components. From the source you can get an accurate understanding of each component’s behavior and API.

The React Native documentation only discusses the components, APIs and topics specific to React Native (React on iOS and Android). For further documentation on the React API that is shared between React Native and React DOM, refer to the [React documentation](http://u.720life.cn/g/2b5f360ced91899e6d7809fb5ee1ea1fbd77b72146743bf5b007101f454a72b88e30e19331249baa2c31ab8d82da80d1 

## Examples

- `git clone https://github.com/facebook/react-native.git`
- `cd react-native && npm install`

### Running the examples on iOS

Now open any example (the `.xcodeproj` file in each of the `Examples` subdirectories) and hit Run in Xcode.

### Running the examples on Android

Note that you'll need the Android NDK installed, see [prerequisites](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046405e3357754798ba3fdb28fb956ae71f424fdb234191f994f1201cd4d17f0d77adf5c7cd9cf8abfe025f7db948617774487edbf764cc7f734f1f721f98fd853bc6e4b705d1099d5fade6d4f37a8f475a 

```bash
./gradlew :Examples:Movies:android:app:installDebug
# Start the packager in a separate shell (make sure you ran npm install):
./packager/packager.sh
# Open the Movies app in your emulator
```

## Extending React Native

- Looking for a component? [JS.coach](http://u.720life.cn/g/fbd7b5d1da7fb6bde6bf3128ee5fa2f6ce9c3c59b143bd69375d9c610c9c2bbd) 
- Fellow developers write and publish React Native modules to npm and open source them on GitHub.
- Making modules helps grow the React Native ecosystem and community. We recommend writing modules for your use cases and sharing them on npm.
- Read the guides on Native Modules ([iOS](http://u.720life.cn/g/2b5f360ced91899e6d7809fb5ee1ea1fbd77b72146743bf5b007101f454a72b83b8b2fd7b388e483b123ca1049289a89d854bd5c2f7919ca310e5aa84489a098561f988c54e6ce753b3268a1df2e5f90  [Android](http://u.720life.cn/g/2b5f360ced91899e6d7809fb5ee1ea1fbd77b72146743bf5b007101f454a72b83b8b2fd7b388e483b123ca1049289a89e7e10e8bcdd526de0ab140a3960e1154cdf66f80d7afb0d0be6e327cd32aa013)  and Native UI Components ([iOS](http://u.720life.cn/g/2b5f360ced91899e6d7809fb5ee1ea1fbd77b72146743bf5b007101f454a72b83b8b2fd7b388e483b123ca1049289a891eb4d925fbcf6f260bddf70b3fd96aa0cbb13cd4b4df9fadd1160d462e39dc82  [Android](http://u.720life.cn/g/2b5f360ced91899e6d7809fb5ee1ea1fbd77b72146743bf5b007101f454a72b83b8b2fd7b388e483b123ca1049289a895ff8fc0bfe82009af897a875388f5ad9e511988ad55aaac5ae52fce6e6c1f4aa)  if you are interested in extending native functionality.

## Upgrading

React Native is under active development. See the guide on [upgrading React Native](http://u.720life.cn/g/2b5f360ced91899e6d7809fb5ee1ea1fbd77b72146743bf5b007101f454a72b847042691c206a0625d074ebbd23b38c3898435d15fc0934e23f2d0d5a400287e)  to keep your project up-to-date.

## Opening Issues

If you encounter a bug with React Native we would like to hear about it. Search the [existing issues](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046405e3357754798ba3fdb28fb956ae71fe5dd73c518ad2b534ddcd1f1b9cb0332)  and try to make sure your problem doesn’t already exist before opening a new issue. It’s helpful if you include the version of React Native and OS you’re using. Please include a stack trace and reduced repro case when appropriate, too.

The GitHub issues are intended for bug reports and feature requests. For help and questions with using React Native please make use of the resources listed in the [Getting Help](#getting-help) section. [Product Pains](http://u.720life.cn/g/27a80ee59655d78d4485b61b75d0940c16a1ae56057dc4df753df363ec9249553b729e07b6ebd048a0293f8a1ff417ba)  in particular is a good way to signal your interest in a feature or issue. There are limited resources available for handling issues and by keeping the list of open issues lean we can respond in a timely manner.

## Contributing

For more information about contributing PRs and issues, see our [Contribution Guidelines](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046405e3357754798ba3fdb28fb956ae71f424fdb234191f994f1201cd4d17f0d77ebdca09418ae7ee7156f14cce223d476e9ca0d72f2aad2bea5ed63f51b9a23cd 

[Good First Task](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046405e3357754798ba3fdb28fb956ae71ff67289b020f6a5e900b73f5ae045f1230e083026268b218ddfc00caa0fecabe649ebdb511ec5d0d1f4e6fe1a52c99082)  is a great starting point for PRs.

We encourage the community to ask and answer questions on Stack Overflow with [the react-native tag](http://u.720life.cn/g/87bbd50441ad714fa4b3a92b06a39057c99d561856c3866c7b363085c26fdd7b6d75b0ffabc0815b9f4120488ac57f2331f1f63bed7cebcd8c89665a7f7892c9  It's a great way to help out and be involved!

## License

React is [BSD licensed](./LICENSE). We also provide an additional [patent grant](./PATENTS).

React documentation is [Creative Commons licensed](./LICENSE-docs).

Examples provided in this repository and in the documentation are [separately licensed](./LICENSE-examples), as are some of the [custom components](./LICENSE-CustomComponents).



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)