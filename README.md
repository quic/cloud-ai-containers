## Contents

This repository contains docker images useful for QAIC devices.  They expect
that the Platform SDK (at least the driver and firmware) is installed on
the host.

Images are shown under the "Packages" section of this repository.
Associated versions and pull commands are there.

The images contained are:

- cloud_ai_inference_pytools:
  This image is useful for performing inferences and working with models.
  It's able to compile models for, and execute models on AIC100 cards.
  It contains the Apps SDK, Platform SDK, and various python-based tools
  useful for working with and compiling models and executing inferences.
  It has pytools for CV type models rather than QEfficient and vllm for
  language models as the other images do.
  Entrypoint: /bin/bash

- cloud_ai_inference_rh_ubi9:
  This image is useful for performing inferences and working with models.
  It's able to compile models for, and execute models on AIC100 cards.
  It contains the Apps SDK, Platform SDK, and various python-based tools
  useful for working with and compiling models and executing inferences.
  It's based on Red Hat's UBI9 base image.
  Entrypoint: /bin/bash

- cloud_ai_inference_rh_ubi9_vllm_tgis:
  This image is useful for performing inferences and working with models.
  It's able to compile models for, and execute models on AIC100 cards.
  It contains the Apps SDK, Platform SDK, and various python-based tools
  useful for working with and compiling models and executing inferences.
  It's based on Red Hat's UBI9 base image.  Additionally it has the
  vllm_tgis_adapter package installed.
  Entrypoint: /bin/bash

- cloud_ai_inference_rh_ubi9_vllm_085_tgis:
  This image is similar to cloud_ai_inference_rh_ubi9_vllm_tgis, but with
  vllm v0.8.5 installed.
  Entrypoint: /bin/bash

- cloud_ai_inference_ubuntu22:
  This image is useful for performing inferences and working with models.
  It's able to compile models for, and execute models on AIC100 cards.
  It contains the Apps SDK, Platform SDK, and various python-based tools
  useful for working with and compiling models and executing inferences.
  It's based on Ubuntu 22.04.
  Entrypoint: /bin/bash

- cloud_ai_inference_ubuntu24:
  This image is useful for performing inferences and working with models.
  It's able to compile models for, and execute models on AIC100 cards.
  It contains the Apps SDK, Platform SDK, and various python-based tools
  useful for working with and compiling models and executing inferences.
  It's based on Ubuntu 24.04.
  Entrypoint: /bin/bash

- cloud_ai_inference_vllm:
  This image is similar to cloud_ai_inference_ubuntu24, but with a vllm
  entrypoint defined.
  Entrypoint: python3 -m vllm.entrypoints.openai.api_server

- cloud_ai_inference_vllm_085:
  This image is similar to cloud_ai_inference_ubuntu24, but with vllm v0.8.5
  and a vllm entrypoint defined.
  Entrypoint: python3 -m vllm.entrypoints.openai.api_server

- cloud_ai_inference_vllm_disagg:
  This image is similar to cloud_ai_inference_vllm, but with a qaic-disagg
  entrypoint defined.
  Entrypoint: python3 -m qaic_disagg

- cloud_ai_inference_vllm_085_disagg:
  This image is similar to cloud_ai_inference_vllm_085, but with a qaic-disagg
  entrypoint defined.
  Entrypoint: python3 -m qaic_disagg

- cloud_ai_inference_vllm_qaic_pyt:
  This image is useful for performing inferences and working with models.
  It's able to compile models for, and execute models on AIC100 cards.
  It contains vLLM and PyTorch in eager mode.
  It contains the Apps SDK, Platform SDK, and is based on Ubuntu 24.04.
  Entrypoint: python3 -m vllm.entrypoints.openai.api_server

- cloud_ai_k8s_device_plugin:
  This is a kubernetes device plugin for AIC100 cards.
  Entrypoint: k8s-device-plugin

- cloud_ai_mgmt_aicm:
  This is an image which runs the AIC Manager application.
  Entrypoint: python3 aicm_agent.py --ip=0.0.0.0 -vv

- cloud_ai_mgmt_qmonitor:
  This is an image which runs the QMonitor application.
  Entrypoint: /opt/qti-aic/tools/qaic-monitor-grpc-server -v

- cloud_ai_triton_server:
  This image is similar to the inference images, but also contains the Triton Inference Server.
  Entrypoint: /bin/bash

## License
These container images are licensed under the terms in the [LICENSE](LICENSE) file.
By pulling and using these containers, you accept the terms and conditions of this license.

These container images contain open source and other components that are governed by their
own licensing terms.  Refer to those individual components for their licensing terms.
