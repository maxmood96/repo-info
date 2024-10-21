## `amazoncorretto:23-headless`

```console
$ docker pull amazoncorretto@sha256:a8eb30bcaf73455f227c2b8081a7a745344ed33230e0378facbd0eb19e577988
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c7b0f3dda708cafa2db83bb411d5798610b692d95a30cf5fe1babdaf5ce41b5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.4 MB (145416961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdb6d9deda938828fc45fabd9f82af5b3318dec9ca275e9b22eb1d28a0dc6beb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=23.0.1.8-1
# Wed, 16 Oct 2024 02:18:03 GMT
ARG package_version=1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=23.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:42ce99aa0f68a7f3dc752dad87f21431a084b94a3818ff00f932236a9010d564`  
		Last Modified: Tue, 15 Oct 2024 02:06:15 GMT  
		Size: 52.3 MB (52343832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f35755d8f66ac15027316dda0745f0f2a20d833b3c053bb1fa52c4c9be5aeb4c`  
		Last Modified: Mon, 21 Oct 2024 18:57:18 GMT  
		Size: 93.1 MB (93073129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a038600b2f2650cb4c6fc4e0a8af1b895399ffe2df56c405be184a6293ab0fec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5198045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c0117314cdb60612dd3ca0d6322dc6a519c8d6c812d5552c4cee8fcb496df4`

```dockerfile
```

-	Layers:
	-	`sha256:0c69b14fd24a8d6e5a750b3c6f2649dc459d9070d2a4992494bab483c49c7acc`  
		Last Modified: Mon, 21 Oct 2024 18:57:15 GMT  
		Size: 5.2 MB (5188973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37989e0b334e0fce81778363e7abd624e75eb634e90753599dd9d0176b015c46`  
		Last Modified: Mon, 21 Oct 2024 18:57:14 GMT  
		Size: 9.1 KB (9072 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0902304535d8ca0727c8bb6de6e51473bb53d398b51311f557fe6c66edd9c79b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.4 MB (143413040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:193e889d6e158cd23c79c431f28c6dc8013c3a05bf33bf11e361a321c910398f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Oct 2024 16:34:52 GMT
COPY /rootfs/ / # buildkit
# Thu, 03 Oct 2024 16:34:52 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=23.0.1.8-1
# Wed, 16 Oct 2024 02:18:03 GMT
ARG package_version=1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=23.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:9e91bc818827f819b6de2c247e4fed5f971ec9990bc2b6330e067ca2f956815d`  
		Last Modified: Thu, 03 Oct 2024 17:46:58 GMT  
		Size: 51.4 MB (51426364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5715d1f42aae9009f8530d413e085db04bc4c35e797557f00dafa86c66ac6520`  
		Last Modified: Wed, 16 Oct 2024 18:42:16 GMT  
		Size: 92.0 MB (91986676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d7bf3f33f58592c8faaaca15e0c732b4ddc838745cef4eff0237cb7acdacea93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5196168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee3c106283f00bb14aedbd5c0fc3812121a5573c89b517e6b526097e45323c1c`

```dockerfile
```

-	Layers:
	-	`sha256:b06f5b672d1ee715aec551bd595624e9ad5afb349e11425dac33cc7c43c6e7bf`  
		Last Modified: Wed, 16 Oct 2024 18:42:12 GMT  
		Size: 5.2 MB (5187001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7d46b684389ba8725a0a4f4021e5c234cf14c6f922992059520860dfd544508`  
		Last Modified: Wed, 16 Oct 2024 18:42:12 GMT  
		Size: 9.2 KB (9167 bytes)  
		MIME: application/vnd.in-toto+json
