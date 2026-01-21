## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:a11db9ab0320f9ec0e45f0252817564bccc1d5a699efb03a58de039808231995
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:59a94e85d55d700761a2e20804a7f7abe17ba2f95b5f8346948bc30888661136
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (130030210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37e58079d4ef3a452e716ed8bd734fb7b29ea78d306b1f283507e0931a99c6ac`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:45 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 18:59:58 GMT
ARG version=11.0.30.7-1
# Wed, 21 Jan 2026 18:59:58 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 21 Jan 2026 18:59:58 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 18:59:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:ed23be565800a5983cd3d8b6fd581e584110f08d9e32684d0eb5ab2820cadcbc`  
		Last Modified: Wed, 07 Jan 2026 22:09:37 GMT  
		Size: 54.0 MB (54021204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d319609f71d3e24f395b6f673d0f56be309b3e3e0b407c261094ab118c02a4`  
		Last Modified: Wed, 21 Jan 2026 19:00:40 GMT  
		Size: 76.0 MB (76009006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:23b6113a9ea2b4ba5c588dad95c2eaeefe48a22785c437957b41e0e7b9b788f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5205432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be580c7e2aee64ae331ccde3b13f7736478f3605657754bf42bcc673bf3fe24`

```dockerfile
```

-	Layers:
	-	`sha256:d6ce7164ce749e4ddf500fdad89b75666f0b17d5273d4ee41d32154ac482c162`  
		Last Modified: Wed, 21 Jan 2026 19:48:05 GMT  
		Size: 5.2 MB (5196823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3daebd443ae18847a066832a90713516b5b1b7a88b846966556100ae800ec7ed`  
		Last Modified: Wed, 21 Jan 2026 19:48:38 GMT  
		Size: 8.6 KB (8609 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:fa11606f0d5f7cd5a0e23a71f7f1de25d98e6b18b3ce11eb2a63eaff2074d4b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128154643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bce5c8380a91c22df0e230a4334c823cfc9f7b42f5a20b21907e2a9a60cf73ca`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:15 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:15 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 18:59:28 GMT
ARG version=11.0.30.7-1
# Wed, 21 Jan 2026 18:59:28 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 21 Jan 2026 18:59:28 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 18:59:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:60a6ef84e125e61efd6725688f23e752e71a4dd414aa447d2bc3e2a4a5f823e0`  
		Last Modified: Wed, 07 Jan 2026 22:47:36 GMT  
		Size: 52.9 MB (52914357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bec8968a82338ac54e20c0f59f8563d285465f3ccfc3c4b75e19481f059b261`  
		Last Modified: Wed, 21 Jan 2026 19:00:17 GMT  
		Size: 75.2 MB (75240286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:dad5b53c3b6ef5b1e23712c51b6bea667ee415d62c1c9dae79dcdf9cfc268b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5205130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be14b97bdabba575ffe756e4756958b6e353802f22b1d6df42859dadcf5ad9dc`

```dockerfile
```

-	Layers:
	-	`sha256:db385239908eb9218b2d8079e141b5a47e17b8c3b2dc194f911ca222c2235a6b`  
		Last Modified: Wed, 21 Jan 2026 18:59:43 GMT  
		Size: 5.2 MB (5196441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1dae088995febd5740649b81f5a291170e46efaee29f00bf764da6d24f2f8f3`  
		Last Modified: Wed, 21 Jan 2026 19:48:11 GMT  
		Size: 8.7 KB (8689 bytes)  
		MIME: application/vnd.in-toto+json
