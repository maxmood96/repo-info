## `amazoncorretto:22-headless`

```console
$ docker pull amazoncorretto@sha256:e688d4192f9deb366cb02603c576fad9e1cbf055f11a2378766126d0a5364107
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:22-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9e20f91e171cecf1b9350f5a4ee98a29a3610ffe9081acbe63852ec32bfefbb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.7 MB (140663126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7ec6d77fb2738add77a7d6380c83b146f3a36ca01f7d94cbef04cbd65388024`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=22.0.2.9-1
# Tue, 16 Jul 2024 22:56:42 GMT
ARG package_version=1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=22.0.2.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:b60b6c892280988095a2507a148439d3b5fd7b108e66565a91cbdb1f0e543fa0`  
		Last Modified: Mon, 19 Aug 2024 23:08:46 GMT  
		Size: 52.3 MB (52325078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8abd8a34834caac3db01f05ae7314329e66ce512bb7815e50cf0a5f842bf6f85`  
		Last Modified: Fri, 23 Aug 2024 01:50:37 GMT  
		Size: 88.3 MB (88338048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c85897c9718f8efd2d2a991ac859cbeb11bbd8737c62d87a03648200137097d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5196353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75b3e17342111891ba4ef003affb5dfac5387603c593ede91a7c6e3d218fe008`

```dockerfile
```

-	Layers:
	-	`sha256:591817abf437f1188d9a11bb0ae7d9256d10f119d030748757239beeb79426dd`  
		Last Modified: Fri, 23 Aug 2024 01:50:35 GMT  
		Size: 5.2 MB (5187315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0520a952f585ba47846232dfea9b8867e70c52d10482f9c0be226909756fc2e`  
		Last Modified: Fri, 23 Aug 2024 01:50:34 GMT  
		Size: 9.0 KB (9038 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:22-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6958b3e68224a47c742cfebcf6a2f223a3ab24c1469e1b6d3e89145301a4caa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 MB (138716774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65a7c8b82042a29ce883e0d5c6a58ba4d9bf1ad610eb9d30d8fadd05a466c78f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=22.0.2.9-1
# Tue, 16 Jul 2024 22:56:42 GMT
ARG package_version=1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=22.0.2.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:875f26d62c6d0f5a935b0c8548e8375f2a9b98d7669bf434dcd5b36e2114348a`  
		Last Modified: Tue, 20 Aug 2024 01:54:55 GMT  
		Size: 51.4 MB (51426298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673a31234fc406dc3bf1342a961cce5292a58aec8b1a4d24b5a5e81c382f86cd`  
		Last Modified: Fri, 23 Aug 2024 02:38:04 GMT  
		Size: 87.3 MB (87290476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:254c46da6eeeae79d5a9aa26fe65de4b85160517f35444d283e93c1a0b93060c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5194710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd9cd2002f367aeb0707e8ba179567449865e2449d68e1036b43f20fe3a54450`

```dockerfile
```

-	Layers:
	-	`sha256:c16868c905dea7826536a5fccd15b199db4a739dd270725951fe46ddebfec173`  
		Last Modified: Fri, 23 Aug 2024 02:38:02 GMT  
		Size: 5.2 MB (5185299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b376892aab067ca9c02aadc4a49c0a9cd3fc6709a60a3051c2889e4dfa7dfbef`  
		Last Modified: Fri, 23 Aug 2024 02:38:02 GMT  
		Size: 9.4 KB (9411 bytes)  
		MIME: application/vnd.in-toto+json
