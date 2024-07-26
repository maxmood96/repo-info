## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:489ad65bfd0f89253422fa5692f982c575731ce98a001d44449e37008f5464db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4857ceeea89d8c5173725a24c5df72b7b6ce834aaccffbc3d16e44bbe0de82cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 MB (134755813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf3a93e1d333f87ae8028e9e4a818b4f75277e7bbeb70f0293a2e665c0ea6ac`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
ARG package_version=1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:d6f07a4c10a78dc230bb1bc2582e93fdd808a2b79539a9b9e8a29b5a94b2e75a`  
		Last Modified: Tue, 23 Jul 2024 01:08:56 GMT  
		Size: 52.3 MB (52314179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da110cad6efd4f66cedca7ef49c16a211f877b0687a5d85bcfd2c40544d1e71`  
		Last Modified: Thu, 25 Jul 2024 21:02:16 GMT  
		Size: 82.4 MB (82441634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1826698e6d23a5945dbd17c6ff05452e4aa5b1222ad842ce356f1dd0d7e8ed27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5191230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efdf78e486597ecbaf80a2c12829dc1b571040f64a94f86007ed4b6f02ff923f`

```dockerfile
```

-	Layers:
	-	`sha256:aed9e8323204284852f08bc797be95d21dbbc75fe45138ac52920dc898452715`  
		Last Modified: Thu, 25 Jul 2024 21:02:15 GMT  
		Size: 5.2 MB (5182513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8b2eeea1cddf676112008f05b03f5d33e516c377d7fb4123f1beca735717001`  
		Last Modified: Thu, 25 Jul 2024 21:02:15 GMT  
		Size: 8.7 KB (8717 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:dc18d2f6c00795aa9d6148dc524854bdc75cb06cc41afa6a46c0c69a7fe316d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133166364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98ff0d69e0fc83f00bbff386f4658b2a0af674c0edb5a834c0f9b32324bbb18a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
ARG package_version=1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:69f1520adb0e35dcf91717c80b7867ab26fcf8ef8506b9831fcca72a1b38b618`  
		Last Modified: Tue, 23 Jul 2024 01:08:54 GMT  
		Size: 51.4 MB (51402016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ba550945303d3f2b1928447348e3ab84489ccc233019616a176e4fdebc6187`  
		Last Modified: Fri, 26 Jul 2024 01:57:03 GMT  
		Size: 81.8 MB (81764348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d360411fdf30b3a01d823bd985d4e43c6a699177546d169d4af02376d4a7fbaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5190376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3963b4b72078332f2bf9a51e706840fee26dbb503cdc60fedb78b2c167b8e975`

```dockerfile
```

-	Layers:
	-	`sha256:00d795dacff59816c08d53a912580a25562ae119267bf5bd1ac03b16d235f4a4`  
		Last Modified: Fri, 26 Jul 2024 01:57:01 GMT  
		Size: 5.2 MB (5181298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f08912555b73e160d72e465e0326bd03a09f30099625d7e89464575e300b2eb7`  
		Last Modified: Fri, 26 Jul 2024 01:57:00 GMT  
		Size: 9.1 KB (9078 bytes)  
		MIME: application/vnd.in-toto+json
