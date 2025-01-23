## `amazoncorretto:23-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:bae78f9201ef098923f8db85ddec71ea408c3278258462804d4504e5335d90a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:922936e61ff26ff435a65e0e2bc0842582081d2e4c1c68419c172198c858c333
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.3 MB (146273509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b52b09a39def7a8de5189a4bed9495125ee4f7c99752083963cc41ac450a7668`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=23.0.1.8-1
# Fri, 13 Dec 2024 23:01:14 GMT
ARG package_version=1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=23.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:889191eec1e06c30b7664dfba1dba1d3f04b40b1cf6af4214dac90b998f32621`  
		Last Modified: Fri, 10 Jan 2025 02:01:02 GMT  
		Size: 53.2 MB (53150475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab61e0dbdb0a22cd9aa27c0009fdb43b7cd12b67ff740b9d1710efbc1fb3865`  
		Last Modified: Sat, 11 Jan 2025 02:29:43 GMT  
		Size: 93.1 MB (93123034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:049ffa825e1261520ed2b704d050bf2e819aaeed01618a920eb91769d17064a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5192933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c59e3539dcd42987d023266509fde95f4a5b27bca06aa594f615b682e75e5995`

```dockerfile
```

-	Layers:
	-	`sha256:936d054d4df7c5059abb5ce3b10f551ceee8567e8120f108888ce4cfdbbc256f`  
		Last Modified: Sat, 11 Jan 2025 02:29:41 GMT  
		Size: 5.2 MB (5183862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a057694075729c142ed5daf302abadf1796b2091f4ad6417485e69bafa3552e`  
		Last Modified: Sat, 11 Jan 2025 02:29:40 GMT  
		Size: 9.1 KB (9071 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:898811fe10a4a2081627013a429f72fb503f34b3d65300f1414327247b068014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.4 MB (144405850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6f9ac500cb648c49b90342ee83105e0debef0e92b70ea76a07cff344a547cc0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 Jan 2025 23:01:37 GMT
COPY /rootfs/ / # buildkit
# Thu, 09 Jan 2025 23:01:37 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=23.0.2.7-1
# Thu, 23 Jan 2025 01:09:23 GMT
ARG package_version=1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=23.0.2.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:2dc99809e33185161e199db0b479b51cf3fb7470fd27c484aff50bdf9dcb5dab`  
		Last Modified: Fri, 10 Jan 2025 02:14:49 GMT  
		Size: 52.3 MB (52268196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3dfb1f7c04745f4421b033c6ef7acf0dd960f244fa4a8b9153107037e7fd93f`  
		Last Modified: Thu, 23 Jan 2025 18:55:32 GMT  
		Size: 92.1 MB (92137654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b4fa3dceb536c05478545f518adb3fc5b5ef87904ecd3b90d5cb9a8fc8bd1c78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5191014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0e6c8ad35981fbd64a257be35a3c25762bb8b3f0b4d6fa5a2632b95d949b647`

```dockerfile
```

-	Layers:
	-	`sha256:c6dffe0bc597f5418576ca203b46763acfc0e38f70345ce56f4e4404a4cf43b1`  
		Last Modified: Thu, 23 Jan 2025 18:55:30 GMT  
		Size: 5.2 MB (5181851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bffd7596511b7577207a698aa7d96767d63e09984f3cc6097b4755d0d1e6df01`  
		Last Modified: Thu, 23 Jan 2025 18:55:29 GMT  
		Size: 9.2 KB (9163 bytes)  
		MIME: application/vnd.in-toto+json
