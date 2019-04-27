# UE4 Temporal AA Ghosting fix

## Disclaimer
Features in this engine modification are considered experimental and may be modified in future releases.

## Overview

This engine modification adds parameters to mitigate ghosting artifacts. Main idea is to decrease quality of TAA when pixel has big screen space speed. There are two parameters: HighSpeedBlendFactor and MaxSpeed. HighSpeedBlendFactor value will be used to achieve final pixel color when it reaches MaxSpeed parameter. Set HighSpeedBlendFactor to 1.0 will disable TAA for pixels with high screen space speed. You can control  this parameters in ProjectSettings -> Rendering -> DefaultSettings. Also, it is possible to control them through console commands: r.TemporalAA.HighSpeedBlendFactor and r.TemporalAA.MaxSpeed. Default values for this parameters ara 0.2 and 40 respectively


## Getting Started

Just download UnrealEngine-4.22.0 folder from repository and move/replace its contents to your engine folder. You will also have to recompile your engine afterwards. 

### Prerequisites

You have to run you project on UE4 4.22.0 compiled from sources. All prerequisites are the same as for running the usual engine. Merging with later versions of the engine was not tested, however may be possible. Please let us know about your experience in the comments. 

### Roadmap

- Instead of decrease quality we will blend to FXAA PP

## Contributing

Please read [CONTRIBUTING.md](Documentation/CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/fracturedbyte/UE4-MaterialBlending/tags). 

## Authors

* **Gleb Bulgakov** - *Initial coding* - [FracturedByte](https://github.com/BulgakovGleb)
* **Roman Leshchenko** - *Vision and workflow* - [FracturedByte](https://github.com/mazatracker)

See also the list of [contributors](https://github.com/fracturedbyte/UE4-MaterialBlending/contributors) who participated in this project.

## Acknowledgments

* Many thanks for [PurpleBooth](https://gist.github.com/PurpleBooth/) for making templates of [CONTRIBUTION.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) and [README.md](https://gist.github.com/PurpleBooth/109311bb0361f32d87a2) that we've used for this repo
* Inspired by needs of UE4 developers
