This repository contains docker images useful for QAIC devices.  They expect
that the Platform SDK (at least the driver and firmware) is installed on
the host.

Images are shown under the "Packages" section of this repository.
Associated versions and pull commands are there.

The images contained are:

cloud_ai_inference_ubuntu22:
  This image is useful for performing inferences and working with models.
  It's able to compile models for, and execute models on AIC100 cards.
  It contains the Apps SDK, Platform SDK, and various python-based tools
  useful for working with and compiling models and executing inferences.
  It's based on ubuntu22.


## License
These container images are licensed under the terms in the [LICENSE](LICENSE) file.
By pulling and using these containers, you accept the terms and conditions of this license.


