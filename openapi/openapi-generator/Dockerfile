# Copyright 2017 The Kubernetes Authors.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

FROM ghcr.io/kubernetes-client/gen/base:latest 

# Copy required files
COPY openapi-generator/generate_client_in_container.sh /generate_client.sh
COPY preprocess_spec.py /
COPY custom_objects_spec.json /
COPY ${GENERATION_XML_FILE} /generation_params.xml

ENTRYPOINT ["mvn-entrypoint.sh", "/generate_client.sh"]
