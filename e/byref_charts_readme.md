# Helm Charts

The canonical source for Helm charts is the [Helm Hub](http://u.720life.cn/g/bbb717d6a97b6c54daecc14604f6524daae841e348218e14e18ef63146849e01  an aggregator for distributed chart repos.

This GitHub project is the source for Helm `stable` and `incubator` [Helm chart repositories](http://u.720life.cn/g/5840685aca1616a59945b1d3cb12f5eb910f91840afac97de86ec387ce832accd3580a7260dbf6ec9588e6e721de2503ec6ff2e39f8f08548b8cc0f609203d1f  currently listed on the Hub.

For more information about installing and using Helm, see the
[Helm Docs](http://u.720life.cn/g/5d02e49dfff53439f8c01fd3fd34e90fd33f57ddd6fe27caadf976cce17f85e2  For a quick introduction to Charts, see the [Chart Guide](http://u.720life.cn/g/5d02e49dfff53439f8c01fd3fd34e90f8be3522fdf0c438bdfe37dd4bec02173e7c34f0778fc37852abf47c3249762d1 

## Status of the Project

Similar to the [Helm 2 Support Plan](http://u.720life.cn/g/5d02e49dfff53439f8c01fd3fd34e90f41d4c3b0fd16d11c3c580e261e1f4ae629dadae03c5a3cebfffd1e341e963c0a9c3c834a4500db9c78a6c6de61e76ebd0fe7f04459a80fc9ca05f5e4f0e8f3e3  this GitHub project has begun transition to a 1 year "maintenance mode" (see [Deprecation Timeline](#deprecation-timeline) below). Given the deprecation plan, this project is intended for [apiVersion: v1](http://u.720life.cn/g/5d02e49dfff53439f8c01fd3fd34e90f8be3522fdf0c438bdfe37dd4bec02173af9b8477ff0b4d349f31abe87b78a0d26aa0ec3f4b5a5b945f03fbf74e7bfdff)  Charts (installable by both Helm 2 and 3), and not for `apiVersion: v2` charts (installable by Helm 3 only).

### Deprecation Timeline

| | |
| - | - |
| **Nov 13, 2019** | At [Helm 3's public release](http://u.720life.cn/g/5d02e49dfff53439f8c01fd3fd34e90fd5e8a19f7f6054a52be39930ddd827fdc0e71b6462c3cb9b430ba224b17bf853  new charts are no longer accepted to `stable` or `incubator`. Patches to existing charts may continue to be submitted by the community, and (time permitting) reviewed by chart OWNERS for acceptance |
| **Aug 13, 2020** | At 9 months – when Helm v2 goes security fix only – the `stable` and `incubator` repos will be de-listed from the Helm Hub. Chart OWNERS are encouraged to accept security fixes only. ℹ️ _Note: the original date has been extended 3 months to match Helm v2 support. See [COVID-19: Extending Helm v2 Bug Fixes](http://u.720life.cn/g/5d02e49dfff53439f8c01fd3fd34e90fb840c25e1b196f0e67c5c529fedc8db0d7799ee398f5ce10dedc10c919c5e3524c24ff34c8139f7d830ff8ed97568394  |
| **Nov 13, 2020** | At 1 year, support for this project will formally end, and this repo will be marked obsolete |

This timeline gives the community (chart OWNERS, organizations, groups or individuals who want to host charts) 9 months to move charts to new Helm repos, and list these new repos on the Helm Hub before `stable` and `incubator` are de-listed.

Note that this project has been under active development for some time, so you might run into [issues](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304607061cac550d2d20167a78d683e9a8a4e0be193ba1fd313fa73aec6da54b97ce  If you do, please don't be shy about letting us know, or better yet, contribute a fix or feature (within the deprecation timeline of course). Also be aware the repo and chart OWNERS are volunteers so reviews are as time allows, and acceptance is up to the chart OWNERS - you may [reach out](#where-to-find-us) but please be patient and courteous.

## Where to Find Us

For general Helm Chart discussions join the Helm Charts (#charts) room in the [Kubernetes Slack instance](http://u.720life.cn/g/a3925a8cd6dab93060b8efa56eacceed6f09d4c5b10748eb791e9ce249fd980b 

For issues and support for Helm and Charts see [Support Channels](CONTRIBUTING.md#support-channels).

## How Do I Install These Charts?

Just `helm install stable/ `. This is the default repository for Helm which is located at https://kubernetes-charts.storage.googleapis.com/ and is installed by default.

For more information on using Helm, refer to the [Helm documentation](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046bf7e3a20d599b296568ddfbe68374c1db5be584fb92208a669094aaef74fe526 

## How Do I Enable the Stable Repository for Helm 3?

To add the Helm Stable Charts for your local client, run `helm repo add`:

```
$ helm repo add stable https://kubernetes-charts.storage.googleapis.com
"stable" has been added to your repositories
```

## How Do I Enable the Incubator Repository?

To add the Incubator charts for your local client, run `helm repo add`:

```
$ helm repo add incubator https://kubernetes-charts-incubator.storage.googleapis.com
"incubator" has been added to your repositories
```

You can then run `helm search incubator` to see the charts.

## Chart Format

Take a look at the [alpine example chart](http://u.720life.cn/g/54145d0471d91890860f7f8463c030460f281c740d69a0f3870cb9727ddb757684c309e53be7ff12ca2dea0a3ea7c6dda5ed1cb604f780bcc7d2dca9fcc6e68a1ed7ab51f5480bac87e41cc04f425e5d)  for reference when you're writing your first few charts.

Before contributing a Chart, become familiar with the format. Note that the project is still under active development and the format may still evolve a bit.

## Repository Structure

This GitHub repository contains the source for the packaged and versioned charts released in the [`gs://kubernetes-charts` Google Storage bucket](http://u.720life.cn/g/c52c6a161526abefbb795fee00696d8c36f1bca6644666722eea7cdff50c986e5f221abb65721a2fcd5f87c203052509d85f3ea8e36b940c217251ced364dbd1105ca2774a53a689a523958ac1c29e86)  (the Chart Repository).

The Charts in the `stable/` directory in the master branch of this repository match the latest packaged Chart in the Chart Repository, though there may be previous versions of a Chart available in that Chart Repository.

The purpose of this repository is to provide a place for maintaining and contributing official Charts, with CI processes in place for managing the releasing of Charts into the Chart Repository.

The Charts in this repository are organized into two folders:

* stable
* incubator

Stable Charts meet the criteria in the [technical requirements](CONTRIBUTING.md#technical-requirements).

Incubator Charts are those that do not meet these criteria. Having the incubator folder allows charts to be shared and improved on until they are ready to be moved into the stable folder. The charts in the `incubator/` directory can be found in the [`gs://kubernetes-charts-incubator` Google Storage Bucket](http://u.720life.cn/g/c52c6a161526abefbb795fee00696d8c36f1bca6644666722eea7cdff50c986e5f221abb65721a2fcd5f87c203052509d85f3ea8e36b940c217251ced364dbd14e41718bc36924afedd406e40c287858 

In order to get a Chart from incubator to stable, Chart maintainers should open a pull request that moves the chart folder.

## Contributing to an Existing Chart

We'd love for you to contribute to an existing Chart that you find provides a useful application or service for Kubernetes. Please read our [Contribution Guide](CONTRIBUTING.md) for more information on how you can contribute Charts.

Note: We use the same [workflow](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046c300ee84eff0c7ac499f730e5483220f1db516865313227ba4897a3fd89110834cb0437919970f44937f77add76f010859edfd26a35b1a4ed5a1488c46ec8d73e1a8d603f78c4b4f57d97d3e5a11b111 
[License](LICENSE) and [Contributor License Agreement](CONTRIBUTING.md) as the main Kubernetes repository.

## Owning and Maintaining A Chart

Individual charts can be maintained by one or more users of GitHub. When someone maintains a chart they have the access to merge changes to that chart. To have merge access to a chart someone needs to:

1. Be listed on the chart, in the `Chart.yaml` file, as a maintainer. If you need sponsors and have contributed to the chart, please reach out to the existing maintainers, or if you are having trouble connecting with them, please reach out to one of the [OWNERS](OWNERS) of the charts repository.
1. Be invited (and accept your invite) as a read-only collaborator on [this repo](http://u.720life.cn/g/54145d0471d91890860f7f8463c0304627193d2cb98e43bd19a1d302d76707df  This is required for @k8s-ci-robot [PR comment interaction](http://u.720life.cn/g/54145d0471d91890860f7f8463c03046c300ee84eff0c7ac499f730e5483220f1db516865313227ba4897a3fd89110834cb0437919970f44937f77add76f0108d76228c74841cb303d56d1558e8aaee76e258b28f5300d4ca867343ab8fc68ed 
1. An OWNERS file needs to be added to a chart. That OWNERS file should list the maintainers' GitHub login names for both the reviewers and approvers sections. For an example see the [Drupal chart](stable/drupal/OWNERS). The `OWNERS` file should also be appended to the `.helmignore` file.

Once these three steps are done a chart approver can merge pull requests following the directions in the [REVIEW_GUIDELINES.md](REVIEW_GUIDELINES.md) file.

## Trusted Collaborator

The `pull-charts-e2e` test run, that installs a chart to test it, is required before a pull request can be merged. These tests run automatically for members of the Helm Org and for chart [repository collaborators](http://u.720life.cn/g/1f425b0b33da40ebdfbaffd56fc94509ec09346c8015e0ae429751be8b3a78a5399b00f45c69798d5a0d1b3f9c47322754c824d6d198f76b2a8d5b6b37a12200479ed3a850aef8a8f3b54183dc16c7733f079b6ad8b06b368ed222ed1273719d443a7519380867cead654e0f863983fd  For regular contributors who are trusted, in a manner similar to Kubernetes community members, we have trusted collaborators. These individuals can have their tests run automatically as well as mark other pull requests as ok to test by adding a comment of `/ok-to-test` on pull requests.

There are two paths to becoming a trusted collaborator. One only needs follow one of them.

1. If you are a Kubernetes GitHub org member and have your Kubernetes org membership public you can become a trusted collaborator for Helm Charts
2. Get sponsorship from one of the Charts Maintainers listed in the OWNERS file at the root of this repository

The process to get added is:

* File an issue asking to be a trusted collaborator
* A Helm Chart Maintainer can then add the user as a read only collaborator to the repository

## Review Process

For information related to the review procedure used by the Chart repository maintainers, see [Merge approval and release process](CONTRIBUTING.md#merge-approval-and-release-process).

### Stale Pull Requests and Issues

Pull Requests and Issues that have no activity for 30 days automatically become stale. After 30 days of being stale, without activity, they become rotten. Pull Requests and Issues can rot for 30 days and then they are automatically closed. This is the standard stale process handling for all repositories on the Kubernetes GitHub organization.

## Supported Kubernetes Versions

This chart repository supports the latest and previous minor versions of Kubernetes. For example, if the latest minor release of Kubernetes is 1.8 then 1.7 and 1.8 are supported. Charts may still work on previous versions of Kubernertes even though they are outside the target supported window.

To provide that support the API versions of objects should be those that work for both the latest minor release and the previous one.

## Happy Helming in China

If you are in China, there are some problems to use upstream Helm Charts directly (e.g. images hosted on `gcr.io`, `quay.io`, and Charts hosted on `googleapis.com` etc), you can use this mirror repo at https://github.com/cloudnativeapp/charts which automatically sync & replace unavailable image & repo URLs in every Chart.



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)