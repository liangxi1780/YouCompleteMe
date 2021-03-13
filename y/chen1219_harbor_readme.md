# Harbor

[![CI](https://github.com/goharbor/harbor/workflows/CI/badge.svg?branch=master&event=push)](https://github.com/goharbor/harbor/actions?query=event%3Apush+branch%3Amaster+workflow%3ACI+)
[![Coverage Status](https://codecov.io/gh/goharbor/harbor/branch/master/graph/badge.svg)](https://codecov.io/gh/goharbor/harbor)
[![Go Report Card](https://goreportcard.com/badge/github.com/goharbor/harbor)](https://goreportcard.com/report/github.com/goharbor/harbor)
[![CII Best Practices](https://bestpractices.coreinfrastructure.org/projects/2095/badge)](https://bestpractices.coreinfrastructure.org/projects/2095)
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/c8d726c9cfd047ffaf681449d673f246)](https://www.codacy.com/app/goharbor/harbor?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=goharbor/harbor&amp;utm_campaign=Badge_Grade)
[![Nightly Status](https://us-central1-eminent-nation-87317.cloudfunctions.net/harbor-nightly-result)](https://www.googleapis.com/storage/v1/b/harbor-nightly/o)
![CONFORMANCE_TEST](https://github.com/goharbor/harbor/workflows/CONFORMANCE_TEST/badge.svg)
 

|![notification](docs/img/readme/bell-outline-badged.svg)Community Meeting|
|------------------|
|The Harbor Project holds bi-weekly community calls in two different timezones. To join the community calls or to watch previous meeting notes and recordings, please visit the [meeting schedule](http://u.720life.cn/g/54145d0471d91890860f7f8463c030468c793e89df9d7697fdfca4a336f998d8e4be392b4449aca2e3d68b2e6146375e3fae89ba91640553a306872f9c2a51956bf5e70b2efe022d21e01edc7c7ffdcf 

   

**Note**: The `master` branch may be in an *unstable or even broken state* during development.
Please use [releases](http://u.720life.cn/g/54145d0471d91890860f7f8463c030467878602434b412b1453ad0bde2188c9fafad88542146f26c59e0c6076239fbb3)  instead of the `master` branch in order to get a stable set of binaries.

 

Harbor is an open source trusted cloud native registry project that stores, signs, and scans content. Harbor extends the open source Docker Distribution by adding the functionalities usually required by users such as security, identity and management. Having a registry closer to the build and run environment can improve the image transfer efficiency. Harbor supports replication of images between registries, and also offers advanced security features such as user management, access control and activity auditing.

Harbor is hosted by the [Cloud Native Computing Foundation](http://u.720life.cn/g/3eae61f755c4ef4eab2a2f59aab72e16)  (CNCF). If you are an organization that wants to help shape the evolution of cloud native technologies, consider joining the CNCF. For details about who's involved and how Harbor plays a role, read the CNCF
[announcement](http://u.720life.cn/g/ec73c9c498fc4df4b129c314c7c714069a8e0dd6ac30c9c1fde3096bdba58d1db45f943e9efd7743c24e8353c03fd4892b98f120146067efb8d95ed4f5d691c4cef6b737b68c59024ca917435048620f 

## Features

* **Cloud native registry**: With support for both container images and [Helm](http://u.720life.cn/g/5cab730003ff109750d13b01c27e55c5)  charts, Harbor serves as registry for cloud native environments like container runtimes and orchestration platforms.
* **Role based access control**: Users access different repositories through 'projects' and a user can have different permission for images or Helm charts under a project.
* **Policy based replication**: Images and charts can be replicated (synchronized) between multiple registry instances based on policies with using filters (repository, tag and label). Harbor automatically retries a replication if it encounters any errors. This can be used to assist loadbalancing, achieve high availabiliy, and faciliate multi-datacenter deployments in hybrid and multi-cloud scenarios.
* **Vulnerability Scanning**: Harbor scans images regularly for vulnerabilities and has policy checks to prevent vulnerable images from being deployed.
* **LDAP/AD support**: Harbor integrates with existing enterprise LDAP/AD for user authentication and management, and supports importing LDAP groups into Harbor that can then be given permissions to specific projects.  
* **OIDC support**: Harbor leverages OpenID Connect (OIDC) to verify the identity of users authenticated by an external authorization server or identity provider. Single sign-on can be enabled to log into the Harbor portal.  
* **Image deletion & garbage collection**: System admin can run garbage collection jobs so that images(dangling manifests and unreferenced blobs) can be deleted and their space can be freed up periodically.
* **Notary**: Support signing container images using Docker Content Trust (leveraging Notary) for guaranteeing authenticity and provenance.  In additon, policies that prevent unsigned images from being deployed can also be activated.
* **Graphical user portal**: User can easily browse, search repositories and manage projects.
* **Auditing**: All the operations to the repositories are tracked through logs.
* **RESTful API**: RESTful APIs are provided to facilitate administrative operations, and are easy to use for integration with external systems. An embedded Swagger UI is available for exploring and testing the API.
* **Easy deployment**: Harbor can be deployed via Docker compose as well Helm Chart. A Harbor Operator was added recently as well - https://goharbor.io/docs/1.10/build-customize-contribute/e2e_api_python_based_scripting_guide/

## Architecture

For learning the architecture design of Harbor, check the document [Architecture Overview of Harbor](http://u.720life.cn/g/54145d0471d91890860f7f8463c030461ae3d2f91a821a1e36e047b1ca29b7063562a9ee431325b081bd5e7d78656f7706414b6ef882f0cf97828eec8dec1b8583c4e86bddbac1ef2ddbe11f534688c9 

## API

* Harbor RESTful API: The APIs for most administrative operations of Harbor and can be used to perform integrations with Harbor programmatically.
  * Part 1: [New or changed APIs](http://u.720life.cn/g/46b1bb27f1f59b018f365ce2a9db50fc36376fbd02e54eb882848c38e3ad8384cee44af14129c994ec120a41949555605119db2d22e8a46a2d144242383e021349574dce2027a3d21122a6dbea970543791fcd5d2ab2821f1d45e9f62972de046b1a67f6471c86ccb5b90275016c1052) 
  * Part 2: [Legacy APIs](http://u.720life.cn/g/46b1bb27f1f59b018f365ce2a9db50fc36376fbd02e54eb882848c38e3ad8384cee44af14129c994ec120a41949555605119db2d22e8a46a2d144242383e021349574dce2027a3d21122a6dbea970543791fcd5d2ab2821f1d45e9f62972de0479abd98bc572a7b433ac34b3af5ba5c9d0f4937f426fe06bd44c063ff9b59a7d) 

## Install & Run

**System requirements:**

**On a Linux host:** docker 17.06.0-ce+ and docker-compose 1.18.0+ .

Download binaries of **[Harbor release ](http://u.720life.cn/g/54145d0471d91890860f7f8463c030467878602434b412b1453ad0bde2188c9f6562f31bd0c14758d06ce8463fbab615  and follow **[Installation & Configuration Guide](docs/install-config/_index.md)** to install Harbor.

If you want to deploy Harbor on Kubernetes, please use the **[Harbor chart](http://u.720life.cn/g/54145d0471d91890860f7f8463c030461ae3d2f91a821a1e36e047b1ca29b7069de8793672013685c0c2b16e50d9ea59 

Refer to **[User Guide](docs/user_guide.md)** for more details on how to use Harbor.

## OCI Distribution Conformance Tests

Check the OCI distribution conformance tests [report](http://u.720life.cn/g/6b8381a0f346a49d58454a5f95046f72cf577a5d0298c536573bfa85fc84b1d86555c74b77c2a0bf5a18554a529a96a0ae2705b777402329a2406420e928c92619bf09d8a4dd6594e543102841f6ab9f)  of Harbor.

## Compatibility

The [compatibility list](./docs/install-config/harbor-compatibility-list.md) document provides compatibility information for the Harbor components.

* [Replication adapters](./docs/install-config/harbor-compatibility-list.md#Replication-Adapters)
* [OIDC adapters](./docs/install-config/harbor-compatibility-list.md#OIDC-Adapters)
* [Scanner adapters](./docs/install-config/harbor-compatibility-list.md#Scanner-Adapters)

## Community

* **Twitter:** [@project_harbor](http://u.720life.cn/g/5ea88169c4a0fbd169233d52478d54fede938f79b7180d411e34eb38fcffedc01b8c1baadd7542324e7b16ec813fbafc)   
* **User Group:** Join Harbor user email group: [harbor-users@lists.cncf.io](http://u.720life.cn/g/271b428ff5db6a02bf62b483482af8e4008f0ec4dff2e580fab7db628849506f473dd74cebdd86868ac1d5639736c3d9)  to get update of Harbor's news, features, releases, or to provide suggestion and feedback.  
* **Developer Group:** Join Harbor developer group: [harbor-dev@lists.cncf.io](http://u.720life.cn/g/271b428ff5db6a02bf62b483482af8e47985b38e90b2a5dcabb4679e0b94baa903d2a58d4f79a8c90817bcd744c1019e)  for discussion on Harbor development and contribution.
* **Slack:** Join Harbor's community for discussion and ask questions: [Cloud Native Computing Foundation](http://u.720life.cn/g/724b40f283df6dd96f6f65b6d8668cb5e28efe6e9b0ddebb2139cd1889c45a51  channel: [#harbor](http://u.720life.cn/g/cf2e57301f8f075daa1dee7029aa84ae4108642e315c50e85c4abbfe0eda04729aee678bed785c9b2826e97a63195911)  and [#harbor-dev](http://u.720life.cn/g/cf2e57301f8f075daa1dee7029aa84ae4108642e315c50e85c4abbfe0eda047274a6f01f7e325d6400498fa904fd7625b43e9a08af3e9b917c00c64c1e5d7098) 

## Demos

* **[Live Demo](http://u.720life.cn/g/b38d9ca9a9c8d4fd6ce528e73dbcc45457827733c112ab889d0e2a51cd34d9a1  - A demo environment with the latest Harbor stable build installed. For additional information please refer to [this page](docs/demo_server.md).
* **[Video Demos](http://u.720life.cn/g/54145d0471d91890860f7f8463c030461ae3d2f91a821a1e36e047b1ca29b706ee36a33363506ae4a6244846bc5b61b52a4d04b0a32213cdedc281186966073aa4ac895ac941a74498a92b0f2b82b8b4  - Demos for Harbor features and continuously updated.

## Partners and Users

For a list of users, please refer to [ADOPTERS.md](ADOPTERS.md).

## Security

### Security Audit

A third party security audit was performed by Cure53 in October of 2019. You can see the full report [here](docs/security/Harbor_Security_Audit_Oct2019.pdf).

### Reporting security vulnerabilities

If you've found a security related issue, a vulnerability, or a potential vulnerability in Harbor please let the [Harbor Security Team](mailto:cncf-harbor-security@lists.cncf.io) know with the details of the vulnerability. We'll send a confirmation
email to acknowledge your report, and we'll send an additional email when we've identified the issue
positively or negatively.

For further details please see our complete [security release process](SECURITY.md).

## License

Harbor is available under the [Apache 2 license](LICENSE).

This project uses open source components which have additional licensing terms.  The official docker images and licensing terms for these open source components can be found at the following locations:

* Photon OS 1.0: [docker image](http://u.720life.cn/g/ce46a7789a867c84732a8edd85365bef553220b1f143cb165490c40e162fda97d5527c043e683e1dd8be7ec4a916ebef  [license](http://u.720life.cn/g/54145d0471d91890860f7f8463c030467f8dad16cd7191355f7f99767dee550bdf0c37eddd9489725edb60106ccaedd92d6cd184920729e89b403ca7c2e04d0d) 



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)