# Copyright 2022 The MediaPipe Authors.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#      http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

licenses(["notice"])

package(default_visibility = ["//mediapipe/tasks:internal"])

cc_library(
    name = "running_mode",
    hdrs = ["running_mode.h"],
    visibility = ["//visibility:public"],
)

cc_library(
    name = "image_processing_options",
    hdrs = ["image_processing_options.h"],
    visibility = ["//visibility:public"],
    deps = [
        "//mediapipe/tasks/cc/components/containers:rect",
    ],
)

cc_library(
    name = "base_vision_task_api",
    hdrs = ["base_vision_task_api.h"],
    deps = [
        ":image_processing_options",
        ":running_mode",
        "//mediapipe/calculators/core:flow_limiter_calculator",
        "//mediapipe/calculators/tensor:image_to_tensor_calculator_cc_proto",
        "//mediapipe/framework/formats:image",
        "//mediapipe/framework/formats:rect_cc_proto",
        "//mediapipe/tasks/cc/components/containers:rect",
        "//mediapipe/tasks/cc/core:base_task_api",
        "//mediapipe/tasks/cc/core:task_api_factory",
        "//mediapipe/tasks/cc/core:task_runner",
        "//mediapipe/tasks/cc/vision/utils:image_tensor_specs",
        "@com_google_absl//absl/status",
        "@com_google_absl//absl/status:statusor",
        "@com_google_absl//absl/strings",
    ],
)

cc_library(
    name = "vision_task_api_factory",
    hdrs = ["vision_task_api_factory.h"],
    deps = [
        ":base_vision_task_api",
        "//mediapipe/calculators/core:flow_limiter_calculator",
        "//mediapipe/framework:calculator_cc_proto",
        "//mediapipe/tasks/cc/core:task_api_factory",
        "@com_google_absl//absl/status",
        "@com_google_absl//absl/status:statusor",
        "@com_google_absl//absl/strings",
        "@org_tensorflow//tensorflow/lite/core/api:op_resolver",
    ],
)
