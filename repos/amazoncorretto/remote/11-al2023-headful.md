## `amazoncorretto:11-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:16c4e843a2cc698a87bc9e06e912fcd0c117da595ce1e6ae351ceb114c054f0e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:eda18eb11b9a67075e769ed5d82736e04ab8f5b939f9517de99e795558bc3573
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129159075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf035e7a91913f67fcc304716c4c7ec68e249cbbf6e5f7b5394d959fb22a07e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
COPY dir:8edd892881e79c0c11996c1a60e2c04d066537e06bdf88e1def994a6148ea23c in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=11.0.23.9-1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=11.0.23.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:ee5ee70789863a32f444d11d47a2849acfc6089e3e8c78d196f63475ee994293`  
		Last Modified: Thu, 11 Jul 2024 21:19:58 GMT  
		Size: 52.3 MB (52313695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e525ba3bd8506742dff6dce5a158e17985cf62b86e90e8cdb2149bac05f8f43`  
		Last Modified: Thu, 11 Jul 2024 21:49:02 GMT  
		Size: 76.8 MB (76845380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c7ed1b6b93ffc2d2261ae7f3a5104f63acbc8a8370f3c9f9b29e2028cfaebc0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5204021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d588e50f7f4a310ee16f9a4756797ceeb9c519924ca3f853d615cb5bf5d8a5f6`

```dockerfile
```

-	Layers:
	-	`sha256:bca380769ab0c607d14437f39996ed83dc3e1a868cfbe163024c9b00c84f158c`  
		Last Modified: Thu, 11 Jul 2024 21:49:00 GMT  
		Size: 5.2 MB (5195463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5dc4a92bfb6905c618add4022e9715d570780ebc1cf47734288fea18d79918e`  
		Last Modified: Thu, 11 Jul 2024 21:49:00 GMT  
		Size: 8.6 KB (8558 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:125ca941bda4e5d14ba5f2abd474fd077e68520f1fb07f4678920367fac63d8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127408264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82f662bd349f58a43f5f2037ed72b7b24a2787a13f66bcc45b87dc40c8027929`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
COPY dir:220d6cf9a8bc29f51f634eb7049d0f57bb8f90ed9e3e9047cc8b655deba42085 in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=11.0.23.9-1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=11.0.23.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:cbddb8fcc56265c7d316c4886c5874790b5fbdc8ecff1d3b10689482ea2ef29c`  
		Last Modified: Thu, 11 Jul 2024 21:39:41 GMT  
		Size: 51.4 MB (51401138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87102693b2a235dd6ea823116961ad14273d67d10a102219674e7c327d7af34c`  
		Last Modified: Thu, 11 Jul 2024 22:51:41 GMT  
		Size: 76.0 MB (76007126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:03a2d5c3c31bd9719836dbd56f9842bdfdf1775857501cd890a377e421222ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5203921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b5c636f50ed13cab3cb3d2058c70022b994fb7a190043db23d911765d1c3af7`

```dockerfile
```

-	Layers:
	-	`sha256:022d49beeff4d66709d61bf3009e3fe9b6c8685b21a0b7afd323f29d8b2c0423`  
		Last Modified: Thu, 11 Jul 2024 22:51:40 GMT  
		Size: 5.2 MB (5195082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:384260efc48362f4d3149c6edd340989f6d22fa3062fee4fbbc799ce513a3ba7`  
		Last Modified: Thu, 11 Jul 2024 22:51:39 GMT  
		Size: 8.8 KB (8839 bytes)  
		MIME: application/vnd.in-toto+json
