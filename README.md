## Contents

This repository contains docker images useful for QAIC devices.  They expect
that the Platform SDK (at least the driver and firmware) is installed on
the host.

Images are shown under the "Packages" section of this repository.
Associated versions and pull commands are there.

The images contained are:

- cloud_ai_inference_ubuntu22:
  
  This image is useful for performing inferences and working with models.
  It's able to compile models for, and execute models on AIC100 cards.
  It contains the Apps SDK, Platform SDK, and various python-based tools
  useful for working with and compiling models and executing inferences.
  It's based on ubuntu22.

- cloud_ai_k8s_device_plugin:
  
  This image works as a Kubernetes device plugin and provides access to
  Qualcomm Cloud AI devices via Kubernetes.  Full documentation of how to
  use this image, how to reserve devices, and what devices are available is
  part of the apps SDK and associated documentation.


## License
These container images are licensed under the terms in the [LICENSE](LICENSE) file.
By pulling and using these containers, you accept the terms and conditions of this license.

These container images contain open source and other components that are governed by their
own licensing terms.  Refer to those individual components for their licensing terms.
