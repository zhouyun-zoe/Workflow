# CITA
In here, we will bulid the whole knowledage framework of CITA, including docs, papers and videos. Moreover, we will introduce how community work together and contributing to CITA. Please notice the timeliness of all the following information.

TODO
[] Add more meetup resources
[] Add a release plan template
[] Add CIP

## What is CITA!

CITA（ Cryptape Inter-enterprise Trust Automation ）is a smart contract supported blockchain framework, aiming to provide a stable, efficient, flexible and future-oriented platform for enterprise-level blockchain applications. In CITA, functionalities of a blockchain node are decoupled into six microservices, including RPC, Auth, Consensus, Chain, Executor，Network. Microservices coordinate with each other via message queue. By configuring and customizing the services, CITA can meet all the needs of enterprise users.

By now, you may wonder What exactly is CITA and how to build your own blockchain network. Check [CITA Docs](https://docs.nervos.org/cita/#/zh/develop/) for the first. In here, you can get into know:

* [How to set up a simple CITA network](https://docs.nervos.org/cita/#/chain/getting_started)
* [How to config your blockchain network](https://docs.nervos.org/cita/#/chain/config_tool)
* [How to use contracts and tools to manage the system](https://docs.nervos.org/cita/#/system_management/contracts)
* [Gain insight into the architecture of CITA](https://docs.nervos.org/cita/#/architecture/architecture)

If you want to build your own application on CITA, here is the [detailed guide](https://docs.nervos.org/nervos-appchain-docs/#/quick-start/build-dapp). And there are some [demo Dapps](https://github.com/cryptape/dapp-demos).

Other Resources (paper, podcast, videos)

* what is permissioned blockchain and what is public permissioned blockchain?
  * [未来是公有链会成功还是联盟链会成功](https://www.jianshu.com/p/db019fbb14b7)
* why we choose to make CITA as a permissioned blockchain?
  * [为什么我们需要另外一种区块链](https://www.jianshu.com/p/db019fbb14b7)
* why we choose to make CITA can also as a public permissioned blockchain?
  * [如何在数字世界实现信任的自动化？](https://www.jianshu.com/p/ff00ca99499a)
* why we choose microservices?
  * [CITA 架构与云计算服务](https://mp.weixin.qq.com/s?__biz=MzUzNjEyNjMzMw==&mid=2247483718&idx=1&sn=abab513ae41d210c293d515524278f71&chksm=fafbb754cd8c3e42140c581922bfef7ced65b1db3575dad5ef1f01a11f9c859c9460bdd8c908&token=1057901215&lang=zh_CN#rd)
  * [演讲实录 | Jan：CITA 与许可链架构（上）](https://mp.weixin.qq.com/s?__biz=MzUzNjEyNjMzMw==&mid=2247483764&idx=1&sn=ed6ce603731ff478157a531ef1cc0d55&chksm=fafbb766cd8c3e703030355d4c0f44d831e3e3aa61ac39879f996df3375844cae8d794c6fb6c&token=1057901215&lang=zh_CN#rd)
  * [演讲实录 | Jan：CITA 与许可链架构（下）](https://mp.weixin.qq.com/s?__biz=MzUzNjEyNjMzMw==&mid=2247483771&idx=1&sn=df42a2dc15e2d76cf7619b426a047d6c&chksm=fafbb769cd8c3e7f2c89870dd3f273aaca30ac55235e38983821df17c2b9aade1a29359f2927&token=1057901215&lang=zh_CN#rd)
* Gain insight into the architecture of CITA
  * [P2P 的网络思考](https://mp.weixin.qq.com/s?__biz=MzUzNzg4NTAzOA==&mid=2247484504&idx=1&sn=70791e666b9ed99c358be12df2ab2618&chksm=fae16459cd96ed4f61f85e0b1568db4d1505504b0e57776021c119ffd11b397838c97d941003&token=1398524652&lang=zh_CN#rd)
  * Coming soon
* Gain insight into the algorithm, logic and code in CITA
  * Coming soon
  
## Contributing Changes

Read [contributing.md](https://github.com/cryptape/cita/blob/develop/CONTRIBUTING.md) for the first.

Please keep in mind nor is code the only way to contribute to the project, we strongly value documentation and gladly accept improvements to the documentation.

### Overview

Generally, CITA uses:

* Github issue and Github Project to create, organize and track logical issues, including bugs and improvements
* CITA improvement proposal for planning major changes
* Github wiki for documentation 
* Github pull requests to manage the review and merge of specific code or docs changes

That is, Github issue and CIP are used to describe what should be fixed or changed, and high-level approaches, and pull requests describe how to implement that change in the project's source code.

* Github Issue

  * Find the existing CITA issue that the change pertains to.
    * Do not create a new issue if creating a change to address an existing issue in GitHub; add to the existing discussion  and work instead.
    * To avoid conflicts, assign the issue to yourself if you plan to work on it.
    * Look for existing pull requests that are linked from the issue, to understand if someone is already working on it.
  * If the change is new, then it usually needs a new issue. However,sometimes，trivial changes, do not require a GitHub issue. Example: "Fix typos in getting started doc"
  * If required, create a new issue (below shows some critical fields to fill-in, a more detailed guidance can be found [here](https://github.com/cryptape/cita/blob/develop/CONTRIBUTING.md):
    * Provide a descriptive Title. 
    * Write a detailed Description. For bug reports, this should ideally include a short reproduction of the problem. For new features, it may include a design document (or a CITA Improvement Proposal if it's a major change).
    * Set required fields: Type, Priority, and optionally Labels. 
    * To avoid conflicts, assign the issue to yourself if you plan to work on it. Leave it unassigned otherwise.
    * Do not include a patch file; pull requests are used to propose the actual change.
  * If the change is a large change, consider inviting discussion on the issue at dev@cryptape.com first before proceeding to implement the change. Note that changes that modify CITA protocols will also require CIP (CITA Improvement Proposal) process.

* Github Pull Request
  Follow the guidance in [Contributing.md](https://github.com/cryptape/cita/blob/develop/CONTRIBUTING.md)

* The Review Process
  * Lively, polite, rapid technical debate is encouraged from everyone in the community. The outcome may be a rejection of the entire change.
  * Try to be responsive to the discussion rather than let days pass between replies.
  * Please add a comment and "@" the reviewer in the PR if you have addressed reviewers' comments. Even though GitHub sends notifications when new commits are pushed, it is helpful to know that the PR is ready for review once again.
  * Sometimes, other changes will be merged which conflict with your pull request's changes. The PR can't be merged until the conflict is resolved. 
  * Add [skip ci] into your commit message when contributing docs.

* Closing Your Pull Request
  * If your pull request is ultimately rejected, please close it.
  * If a pull request has gotten little or no attention, consider improving the description or the change itself and ping likely reviewers again after a few days. Consider proposing a change that's easier to include, like a smaller and/or less invasive change.
  * If a pull request is closed because it is deemed not the right approach to resolve a issue, then leave the issue open. However if the review makes it clear that the issue identified in the issue is not going to be resolved by any pull request (not a problem, won't fix) then also resolve the issue.

## Release

CITA adopted a time based release cadence.

### Future Release Plan
* v0.21 - Dec 2018
  * [Release Plan]()
  * [Current Progress]()
* v1.0 - Feb 2019
  * [Release Plan]()
  
### Older Release

We release in [Github](https://github.com/cryptape/cita/releases).

### Release Process

Check the whole [Release process](https://github.com/zhouyun-zoe/Workflow/blob/master/release%20process.md) for CITA. 
In this process, developers and reviewers decide in advance what release they are aiming for with specific features, Users know when to expect their features. Enough time after feature development will let us test more, document more and resolve more bug issues. Generally, A quicker feedback cycle and users can benefit from features shipped quicker.

#### Who Manages The Releases?
As usual, a committer shall volunteer as release master(RM).

#### What About Version Numbers?
Since the first release in 2017, our current versioning protocol is the following:
We will use three digits for the version: major.minor.bug-fix. The first digit would indicate the major revision (starting at 0), and second indicating minor revision, and the last one number indicating the bug-fix revision.
 
Feature releases will be a minor release by default (i.e. we will only bump up the minor revision digit) unless:
* We break compatibility.
* We do something totally amazing (Just a whisper, 2.0 is on the way ) and decide to release as a new major version milestone.
In those cases, we will bump the major revision digit.

### Component maintainer
What is a maintainer?
All the committers own the CITA code base and should be committed to making it all as good as possible. But we want to ensure that major areas have at least one person (and preferably two) who act as the defacto owners for each logical subsystem. The responsibilities of a maintainer are the following:
* Review code contributions that effect your area as promptly as possible
* Provide the final word on API design for this system
* Act as the point-of-contact for questions from users and other committers that relate to this system
* Have a hygene-related roadmap of items to help make this area of the code base shiny and beautiful. This includes the following:
  * Code quality: prettiness, readability, etc
  * Documentation
  * Test coverage and test quality
* Help triage bugs related to your area of expertise

**Component Maintainers**

| Component | Mantainer | Notes |
| :------| ------: | :------: |
| Chain |  |  |
| Consensus |  |  |
| Network |  |  |
| Executor |  |  |
| Auth |  |  |
| RPC |  |  |



