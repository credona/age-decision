<h1>Research and References</h1>

This document tracks model, dataset and research references used by the Age Decision ecosystem.

Model-specific implementation details remain in the repositories that use them.

<hr>

<h2>Face detection</h2>

Age Decision Core currently uses YuNet for face detection.

Reference:

- OpenCV Zoo - YuNet face detection
- https://github.com/opencv/opencv_zoo/tree/main/models/face_detection_yunet

Notes:

- YuNet is a lightweight face detection model published through OpenCV Zoo.
- The model is used for face localization, not identity recognition.

<hr>

<h2>Age estimation</h2>

Age Decision Core currently uses an ONNX age estimation model.

The current implementation is designed to support multiple ONNX output formats.

Related architecture reference:

- MobileNetV2: Inverted Residuals and Linear Bottlenecks
- https://arxiv.org/abs/1801.04381

Notes:

- Age estimation is probabilistic.
- The output should not be interpreted as proof of real age.
- Calibration and benchmark documentation must remain explicit.

<hr>

<h2>Face anti-spoofing</h2>

Age Decision AntiSpoof currently uses MiniFASNet-style inference and image heuristics.

General field reference:

- Deep Learning for Face Anti-Spoofing: A Survey
- https://arxiv.org/abs/2106.14948

Dataset reference:

- CelebA-Spoof: Large-Scale Face Anti-Spoofing Dataset with Rich Annotations
- https://arxiv.org/abs/2007.12342

Notes:

- Anti-spoofing is not equivalent to certified liveness.
- Still-image anti-spoofing has known limitations against advanced replay and injection attacks.
- Larger and more diverse validation datasets are needed before strong production claims.

<hr>

<h2>Benchmark transparency</h2>

Benchmark claims should clearly separate:

- upstream model claims
- local project validation
- synthetic tests
- integration tests
- production performance

<hr>

<h2>Scientific limitations</h2>

Age estimation and anti-spoofing models may be affected by:

- image quality
- lighting
- camera sensor
- compression
- demographic bias
- pose and occlusion
- domain shift
- adversarial or replay attacks

These limitations must remain visible in public documentation.
