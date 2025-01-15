## `amazoncorretto:23-headless`

```console
$ docker pull amazoncorretto@sha256:1567c23c4546f7091f8f1a1600bc03172347cd25ed955f09c3529fc6a4bdcc3b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-headless` - linux; amd64

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
		Last Modified: Tue, 14 Jan 2025 21:10:26 GMT  
		Size: 93.1 MB (93123034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-headless` - unknown; unknown

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

### `amazoncorretto:23-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:3265faab4c3b215b8fad40b0833bdaf6501c10bddc286a67a579006c00146530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.4 MB (144359712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2519757bddbf8932fb864a88715cb33cf5ff6492d6b5d00a15e66dd15083bf75`
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
	-	`sha256:2dc99809e33185161e199db0b479b51cf3fb7470fd27c484aff50bdf9dcb5dab`  
		Last Modified: Tue, 14 Jan 2025 20:39:04 GMT  
		Size: 52.3 MB (52268196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72887a1fe9202534d9c1a6ef6da7d8779f93c08e13de3e657cd439e0b2a35c10`  
		Last Modified: Sat, 11 Jan 2025 03:13:25 GMT  
		Size: 92.1 MB (92091516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d27a3a7bf428a038f169e4057c948fa3da98d55faec05d326977e5add0208f29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5191012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda955314c16238ab911765124291e54fb0e0f6061975ee1de7ab0a093a77021`

```dockerfile
```

-	Layers:
	-	`sha256:c631a2bfe63f4a0f1fdce9f1a7f5d77316037ded9486ae61bf118ce5f681d9aa`  
		Last Modified: Sat, 11 Jan 2025 03:13:23 GMT  
		Size: 5.2 MB (5181851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9608c9d880bee95c3ed8d637a50b4b636a13196e37d307e6336785f660967119`  
		Last Modified: Sat, 11 Jan 2025 03:13:22 GMT  
		Size: 9.2 KB (9161 bytes)  
		MIME: application/vnd.in-toto+json
