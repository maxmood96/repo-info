## `amazoncorretto:22-jdk`

```console
$ docker pull amazoncorretto@sha256:bc45b73c12f5b969d882f69870e76519588990009f5b79c20d1b1cebd10670b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:22-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:385b21fa4886ca91a5bd86a9cd213855e32f1ebdab07caec7496b75ef952f645
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.9 MB (220930279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:642c7d0917f090590643ea4ac7ce58f53059e9257c0b6635279e1415c18c33f7`
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
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-22-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-22-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-22-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:d6f07a4c10a78dc230bb1bc2582e93fdd808a2b79539a9b9e8a29b5a94b2e75a`  
		Last Modified: Tue, 23 Jul 2024 01:08:56 GMT  
		Size: 52.3 MB (52314179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43a12385dd2bbe4cfa1eee07858c7f47e6afd3b83cd7132cabefe94636214be`  
		Last Modified: Thu, 25 Jul 2024 21:02:22 GMT  
		Size: 168.6 MB (168616100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ec3be201bf8c21b3a60637c57ab5740db877bed36cc697faba234e22ac511ee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5328860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:958636f807f6e755d5c3d65c825f6ae439d441c086bc966bd9526061da13b030`

```dockerfile
```

-	Layers:
	-	`sha256:9fe438d8f8d319d1f94e56e407d07df9a60cb1b7a770988125b7da59bd9e7c83`  
		Last Modified: Thu, 25 Jul 2024 21:02:20 GMT  
		Size: 5.3 MB (5318656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d1bdcc6afa41849ea2d984f3ea6750c20d2f90585dc2108eb56ac63074aa4df`  
		Last Modified: Thu, 25 Jul 2024 21:02:20 GMT  
		Size: 10.2 KB (10204 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:22-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a61d997078f51cc211c24a4314b05b8fcbbc60c058663c255f8116212d7edb6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.0 MB (218024017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51aacb4e2ba9073647158dead7d6c84357b791478602a79ad28584cce43c8288`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Jul 2024 21:39:24 GMT
COPY dir:220d6cf9a8bc29f51f634eb7049d0f57bb8f90ed9e3e9047cc8b655deba42085 in / 
# Thu, 11 Jul 2024 21:39:24 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=22.0.2.9-1
# Tue, 16 Jul 2024 22:56:42 GMT
ARG package_version=1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=22.0.2.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-22-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-22-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-22-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:cbddb8fcc56265c7d316c4886c5874790b5fbdc8ecff1d3b10689482ea2ef29c`  
		Last Modified: Thu, 11 Jul 2024 21:39:41 GMT  
		Size: 51.4 MB (51401138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23651f5270f31387909d75d74e78eb3129501c973418b9895650bf5dbf42e409`  
		Last Modified: Thu, 18 Jul 2024 01:26:18 GMT  
		Size: 166.6 MB (166622879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fc50567f0a988f0441843848b0ff2f885bfc22adceaff17095a8a40b935ef738
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5327120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58944bc51d947154634b85b49d670441c5c1132d069d435cc6a66091364d12e5`

```dockerfile
```

-	Layers:
	-	`sha256:e7e5a424a4ea1dc626c75678af873a60d69c16619e7d0e1ffb2e58c88988db6f`  
		Last Modified: Thu, 18 Jul 2024 01:26:15 GMT  
		Size: 5.3 MB (5316795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3579590c79b59fc399ca90829ad9754e43ba01f5c972afcf13ef0ce327eeee55`  
		Last Modified: Thu, 18 Jul 2024 01:26:14 GMT  
		Size: 10.3 KB (10325 bytes)  
		MIME: application/vnd.in-toto+json
