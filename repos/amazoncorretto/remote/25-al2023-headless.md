## `amazoncorretto:25-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:b17655c7477875f49452a4fd4e78b56304d050964d8a6706afe9dd8fd35ab9a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ed34952134aa600d5477828c2d1b4d744dab65ff8b2d37c66b1301f5908c37ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157607542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5923aedea946eebc9edc5a83418d14dc849079712aba372e3d8296600c10c023`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Sep 2025 20:09:20 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Sep 2025 20:09:20 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=25.0.0.36-2
# Wed, 17 Sep 2025 00:23:53 GMT
ARG package_version=1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=25.0.0.36-2 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:b6baa302384dc877580d7e1080dcca1ed66d9d3b38afc9fcc29c360239e3e362`  
		Last Modified: Tue, 16 Sep 2025 20:50:40 GMT  
		Size: 54.0 MB (54005280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c911cae2c9ca3a3ef69b682fb8982fd5fa035b3313141ac92d7774f61e915d6`  
		Last Modified: Thu, 25 Sep 2025 02:17:26 GMT  
		Size: 103.6 MB (103602262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d555e57cb4f1e41332dfc291c8730d7df8a4b66de763a20004f2acd6a27491eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5203777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6616fe1694efe3e0ce612251dcc3122e31fe4bd6100ad8627ef243f67bab150`

```dockerfile
```

-	Layers:
	-	`sha256:a10b3c6caef191b773ba3e110dd3a89ea6c08fa019751943cca03658572afa77`  
		Last Modified: Thu, 25 Sep 2025 03:52:01 GMT  
		Size: 5.2 MB (5194703 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3acf62a74babd4d974a85f970aa10156bd7ba63a42de7380d1ede9093d080b20`  
		Last Modified: Thu, 25 Sep 2025 03:52:02 GMT  
		Size: 9.1 KB (9074 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b2a69ae8562c196e041665d7a9290d2e142c3296650b28f07ab4759f41686dde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155420797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e8781a8871921f23a2c243d61167c786518c32f48cc95043bec6d95572a96ac`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Sep 2025 20:09:25 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Sep 2025 20:09:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=25.0.0.36-2
# Wed, 17 Sep 2025 00:23:53 GMT
ARG package_version=1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=25.0.0.36-2 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:202438f011bd656c28426fbd92ff7e7030b77e67ebafd3bec95dbce9626db73c`  
		Last Modified: Tue, 16 Sep 2025 22:16:03 GMT  
		Size: 52.9 MB (52899438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a947683b9450efa6133179a9bd1d67b0fafdab609ac7682028534b25ffc4c4f`  
		Last Modified: Thu, 25 Sep 2025 06:11:34 GMT  
		Size: 102.5 MB (102521359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:944fef1f39719a240886706f9918f7eb105f75b746a774bea7834364614a2371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5202680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da4a5701fc3e2d4f813fa7f7b7f8658724bbb4aa4e95dfb6179a6cec7b525d64`

```dockerfile
```

-	Layers:
	-	`sha256:7addacd92c64fb15d734a479a712480a5f2569fc2295f448ac189a1d026e23c5`  
		Last Modified: Thu, 25 Sep 2025 03:52:07 GMT  
		Size: 5.2 MB (5193514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:403f03f57c5686264f71bff9a48d18799b9a7ec2b71dc5f50c33a51a66d23d78`  
		Last Modified: Thu, 25 Sep 2025 03:52:08 GMT  
		Size: 9.2 KB (9166 bytes)  
		MIME: application/vnd.in-toto+json
