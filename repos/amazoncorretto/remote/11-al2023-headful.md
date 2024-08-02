## `amazoncorretto:11-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:05f7b90cb444f69a2ac9eaa8f8de1cfdb6f0ece0b5b99b7f9428ad922a6a2c3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ff9d17c681c3c3f13584a7084fe8accbbba86bf1e303286fcb4a4f997de58460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129166996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fad1adac3167ba750e5329cc65d46b6b897cfc5ddec709564d0e0f4bdbd2597f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=11.0.24.8-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:d6f07a4c10a78dc230bb1bc2582e93fdd808a2b79539a9b9e8a29b5a94b2e75a`  
		Last Modified: Tue, 23 Jul 2024 01:08:56 GMT  
		Size: 52.3 MB (52314179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250e162f1afeff836601a86daeb4383949389ef0272c61f84398662c4166df63`  
		Last Modified: Thu, 25 Jul 2024 21:02:20 GMT  
		Size: 76.9 MB (76852817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:26ce2cf6ecd2f0e88d01dd65eae93eb63c8284dd8660e177b6cc8859c3a937d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5231152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd9a585194999c73130ecf45e511232e26cb97ff64ea03b14c894fe7833f4f27`

```dockerfile
```

-	Layers:
	-	`sha256:705df9af05017f7abad75cdf831bcf71b88658b0f051fa5334056e2fb16f6ca4`  
		Last Modified: Thu, 25 Jul 2024 21:02:18 GMT  
		Size: 5.2 MB (5222398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb96acce0a4152fc4fae6e5e50a19082b1d64788fef51ae8b1411f73d74a94fb`  
		Last Modified: Thu, 25 Jul 2024 21:02:17 GMT  
		Size: 8.8 KB (8754 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:3878a837328a5b14037f7f1da0266c8bd6ecc2ba44c02712156456a76406219f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127411715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9b076a780f5321884abbad4baffd724da3038ae75ef47ca0ab387fc1997862e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=11.0.24.8-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:660e5ad8318bee312fe2855fcd2ace3debe7a81487d99cc02bd0c4e309dbc398`  
		Last Modified: Thu, 01 Aug 2024 21:25:41 GMT  
		Size: 51.4 MB (51402012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632b06976c393839bcd82e2bf2c08477d57f1ef88baefa9224103f856ed179a8`  
		Last Modified: Fri, 02 Aug 2024 05:45:06 GMT  
		Size: 76.0 MB (76009703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:79c5deb5084d2eb27d3532b1d4a1653f835ac78ebe736bb9f55ad66246d0be82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5232213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45d965f93866a02c092f17b272ba097481365c4d4e9104af3dcf0a5c06d3858d`

```dockerfile
```

-	Layers:
	-	`sha256:5aaf434cde2f19e0d7326d7051939d79c56829cf289a342f62150ed6f8cc0f46`  
		Last Modified: Fri, 02 Aug 2024 05:45:04 GMT  
		Size: 5.2 MB (5223098 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:460a1c9810cf07856c1bf2eb1406c62d0e361cd02559b99cd4f7ef4c9c5538b0`  
		Last Modified: Fri, 02 Aug 2024 05:45:03 GMT  
		Size: 9.1 KB (9115 bytes)  
		MIME: application/vnd.in-toto+json
