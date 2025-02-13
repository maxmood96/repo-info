## `ibmjava:8-sfj`

```console
$ docker pull ibmjava@sha256:bdb706af60d4e77f7fbbfb636430ba83f325b750affe77f53ea177dd712ad601
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `ibmjava:8-sfj` - linux; amd64

```console
$ docker pull ibmjava@sha256:8199e58c15991250eef71d14c1929aece3fa929a5663039d1bcd426f5269b200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.2 MB (101242285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7ae93b208b45255ba67eb79e7f6dbc16c82ea92e206386289489ab496e89f0b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 09 Dec 2024 08:06:01 GMT
ARG RELEASE
# Mon, 09 Dec 2024 08:06:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Dec 2024 08:06:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Dec 2024 08:06:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 09 Dec 2024 08:06:01 GMT
ADD file:1b6c8c9518be42fa2afe5e241ca31677fce58d27cdfa88baa91a65a259be3637 in / 
# Mon, 09 Dec 2024 08:06:01 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 08:06:01 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Mon, 09 Dec 2024 08:06:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 08:06:01 GMT
ENV JAVA_VERSION=8.0.8.35
# Mon, 09 Dec 2024 08:06:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3d8f2fbf7a0cdda8ee510bf8fa82df4bbcf08ad707091332b8577ac5cea251bf';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='ede7b25ab451be1f224d95e2ea54e86feb2aaf03c92c8f0eac0773ccd53689d5';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='cceb03a0b74d4c6ddb672f675f7bd44ed6883882204cc6ff3222d607f5718191';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='0600b3689b85b636718e1b5fa59b0d7351c592ddc790968abea3a66b84793e1c';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Mon, 09 Dec 2024 08:06:01 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:9cb31e2e37eab1bff50f727e979fcacb509e225fb853433a6fe21d2fb34e6305`  
		Last Modified: Tue, 04 Feb 2025 05:13:20 GMT  
		Size: 29.5 MB (29535941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d34d794c8b4d6bb1b570ed9c0aa88873abffba40e4960f261d4c2cc59e73641`  
		Last Modified: Tue, 04 Feb 2025 06:50:37 GMT  
		Size: 1.5 MB (1450007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefce767f19e8faaef50033c86e9b302d1ed9ceb6f7a2fa88c354d988acd53a8`  
		Last Modified: Tue, 04 Feb 2025 10:03:01 GMT  
		Size: 70.3 MB (70256337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:c78b90c7a10f26dac691be1200ae71e5d55312d5159b481ee2753999362385e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 MB (2048070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5564886d9e10c24b3c7eabf53421fd93b7d2b84881159e8b690b98e89a260f9`

```dockerfile
```

-	Layers:
	-	`sha256:c751d6a7a9616491ddfc42a5486caa883e78b726ac62185fbf23a187be8ae58f`  
		Last Modified: Tue, 04 Feb 2025 04:42:38 GMT  
		Size: 2.0 MB (2034889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7cdf24370734b4b9c04ce00cab063f0129e3b6fa58eae6bf555db9fdbbc8a8d`  
		Last Modified: Tue, 04 Feb 2025 04:42:37 GMT  
		Size: 13.2 KB (13181 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sfj` - linux; ppc64le

```console
$ docker pull ibmjava@sha256:b3758e50aea93402c1ea3f878d93b7836bf11ebb03b89fa3ff88d0e045ea38d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.1 MB (107063977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9812cc8421f6ec7e81fbeaedffa5a2b83d5eb6b35ba998e1b69f276ec9a166c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 09 Dec 2024 08:06:01 GMT
ARG RELEASE
# Mon, 09 Dec 2024 08:06:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Dec 2024 08:06:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Dec 2024 08:06:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 09 Dec 2024 08:06:01 GMT
ADD file:378a1f28ba6d12429f01a1e40af6c7964a243df3db0827fc9d3841a0e7e3730d in / 
# Mon, 09 Dec 2024 08:06:01 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 08:06:01 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Mon, 09 Dec 2024 08:06:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 08:06:01 GMT
ENV JAVA_VERSION=8.0.8.35
# Mon, 09 Dec 2024 08:06:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3d8f2fbf7a0cdda8ee510bf8fa82df4bbcf08ad707091332b8577ac5cea251bf';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='ede7b25ab451be1f224d95e2ea54e86feb2aaf03c92c8f0eac0773ccd53689d5';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='cceb03a0b74d4c6ddb672f675f7bd44ed6883882204cc6ff3222d607f5718191';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='0600b3689b85b636718e1b5fa59b0d7351c592ddc790968abea3a66b84793e1c';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Mon, 09 Dec 2024 08:06:01 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:2b34fd69ee7e3fb1c28ea96a57188d452075e6a1dc43e3328673c0a828d4cf11`  
		Last Modified: Tue, 04 Feb 2025 07:01:41 GMT  
		Size: 34.4 MB (34447935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549562dbb9f45949b79117ad60c4bbdb1ae9a0fd0a32b6119b57bf804e7f1c77`  
		Last Modified: Mon, 10 Feb 2025 07:38:54 GMT  
		Size: 1.5 MB (1536037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a518d6520db6c53c08a548ecfb405f4ec2e331ceac2b0e0cfcf75576a928b36`  
		Last Modified: Tue, 04 Feb 2025 08:23:32 GMT  
		Size: 71.1 MB (71080005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:a15897cf05afb9c021903daa2283f15e5f46f2da7525a13d6aa5705ba9ea32a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2052491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d1947dd1d9c648288f370ba9017fa2665c4d66a8a1556a1ba24845667bc2d6`

```dockerfile
```

-	Layers:
	-	`sha256:cd1857faec0e1f90f19b411a33c00e5aaf21a957a85495eb62d6182050efe4b6`  
		Last Modified: Tue, 04 Feb 2025 08:23:29 GMT  
		Size: 2.0 MB (2039276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97d4b50258274b52bfe9fd64fe2311a47cb6cf800d1c8a0ac7d84ddbed8bd95f`  
		Last Modified: Tue, 04 Feb 2025 08:23:28 GMT  
		Size: 13.2 KB (13215 bytes)  
		MIME: application/vnd.in-toto+json

### `ibmjava:8-sfj` - linux; s390x

```console
$ docker pull ibmjava@sha256:520e4f652b034824d65e182518c771e9809181dd6b4c23704cfeffb929c87b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.3 MB (100313206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da23bbfb00319c3b9aa92a33ded3f7ab6d6229e3b9aeaf76bb68a1cc0d28dc94`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 09 Dec 2024 08:06:01 GMT
ARG RELEASE
# Mon, 09 Dec 2024 08:06:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 09 Dec 2024 08:06:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 09 Dec 2024 08:06:01 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 09 Dec 2024 08:06:01 GMT
ADD file:39a6583c8b71c00e0ea7562cadb2b343caf5c0c274178520c7476e53faed2e3e in / 
# Mon, 09 Dec 2024 08:06:01 GMT
CMD ["/bin/bash"]
# Mon, 09 Dec 2024 08:06:01 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Mon, 09 Dec 2024 08:06:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Dec 2024 08:06:01 GMT
ENV JAVA_VERSION=8.0.8.35
# Mon, 09 Dec 2024 08:06:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='3d8f2fbf7a0cdda8ee510bf8fa82df4bbcf08ad707091332b8577ac5cea251bf';          YML_FILE='8.0/sfj/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='ede7b25ab451be1f224d95e2ea54e86feb2aaf03c92c8f0eac0773ccd53689d5';          YML_FILE='8.0/sfj/linux/ppc64le/index.yml';          ;;        s390)          ESUM='cceb03a0b74d4c6ddb672f675f7bd44ed6883882204cc6ff3222d607f5718191';          YML_FILE='8.0/sfj/linux/s390/index.yml';          ;;        s390x)          ESUM='0600b3689b85b636718e1b5fa59b0d7351c592ddc790968abea3a66b84793e1c';          YML_FILE='8.0/sfj/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Mon, 09 Dec 2024 08:06:01 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/jre/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
```

-	Layers:
	-	`sha256:7ed94a91c4e77c2e320a028b45fcefc9419c4df2b3d6494bf92ab5d08bba4d77`  
		Last Modified: Tue, 04 Feb 2025 06:45:54 GMT  
		Size: 28.0 MB (28000931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd4605c2f3ea5db01805ac2f6f0f57e95cff85dce667f56133b28c0f20728ce`  
		Last Modified: Fri, 07 Feb 2025 00:58:30 GMT  
		Size: 1.5 MB (1455537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312f9bf3c04d191d1df08b2475e76d5112018d4f38058553a1e2fe0393b5df9e`  
		Last Modified: Thu, 13 Feb 2025 03:21:16 GMT  
		Size: 70.9 MB (70856738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibmjava:8-sfj` - unknown; unknown

```console
$ docker pull ibmjava@sha256:4cdfce1e1d2a187b7b380ae73be4b451e31e31d16a9edc25069acbf608ce9c3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2051682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8be6251aa0ac4960be5c113f97ed40319774c260717a4c5c5ad7dbdde35820fc`

```dockerfile
```

-	Layers:
	-	`sha256:afc5ea06b3e6953b35e9e29f1df26ca5da7b6de47cb516bc2e4e5326364b8cdb`  
		Last Modified: Tue, 04 Feb 2025 08:31:59 GMT  
		Size: 2.0 MB (2038501 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8d85d398a86c7f501bdca8749a5a9e567b5d2f1e05872ac6d6a6adf488cd5bd`  
		Last Modified: Tue, 04 Feb 2025 08:31:59 GMT  
		Size: 13.2 KB (13181 bytes)  
		MIME: application/vnd.in-toto+json
