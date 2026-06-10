## `amazoncorretto:26-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:78629b46214168cc0534a4e86727af439ffd2ce54febdb74fcd1efbaa091f490
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:26-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0fd2747111bafff7c122dffbf74ef7bfba4f6f4875d7af503a8e0337b6a1bf9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.4 MB (160393326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9529fce74262d544f3e909e29f845903f35ceab890a879905080d80d72a14864`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Jun 2026 20:16:24 GMT
COPY /rootfs/ / # buildkit
# Tue, 09 Jun 2026 20:16:24 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 21:12:59 GMT
ARG version=26.0.1.8-1
# Tue, 09 Jun 2026 21:12:59 GMT
ARG package_version=1
# Tue, 09 Jun 2026 21:12:59 GMT
# ARGS: version=26.0.1.8-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 09 Jun 2026 21:12:59 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 21:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
```

-	Layers:
	-	`sha256:c7345fb8c6516aa8699c6c7bbaf8e24d23986ed1d45e3b67479ea9e82b49eb0f`  
		Last Modified: Wed, 27 May 2026 01:40:55 GMT  
		Size: 54.6 MB (54571156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27361122411b991ea55cf048668fcf58d9e9c253b6459e8cf95e1b7026f21a21`  
		Last Modified: Tue, 09 Jun 2026 21:13:20 GMT  
		Size: 105.8 MB (105822170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e30272e9f942a8180066c0d81ed58ac1a61d9c6a02e23a885e0e39f0b73e4fec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5209607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f54c70f3b72658ec47e9b723921958a7e79e5d0004256bb8d93c66c700667118`

```dockerfile
```

-	Layers:
	-	`sha256:c922f75936ddf9137ea4db5ecb45ade8501f289d8327f9e1512943a37ee6250e`  
		Last Modified: Tue, 09 Jun 2026 21:13:18 GMT  
		Size: 5.2 MB (5200408 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51f35b2d59116b3577476fa5cdda9b44318866eaa93d2a66bc08c46d1c1ef531`  
		Last Modified: Tue, 09 Jun 2026 21:13:17 GMT  
		Size: 9.2 KB (9199 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:26-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f0fc344548f34f4a0e4d332d6e547b404e70f00576791de37970a1794ee65a62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.2 MB (158165786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e692cf4231cc55b77f9d8f8ac6c3959bb2863cfb53b9c9d3819c89fc22c490b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Jun 2026 20:16:21 GMT
COPY /rootfs/ / # buildkit
# Tue, 09 Jun 2026 20:16:21 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 21:13:07 GMT
ARG version=26.0.1.8-1
# Tue, 09 Jun 2026 21:13:07 GMT
ARG package_version=1
# Tue, 09 Jun 2026 21:13:07 GMT
# ARGS: version=26.0.1.8-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-26-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-26-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 09 Jun 2026 21:13:07 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 21:13:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-26-amazon-corretto
```

-	Layers:
	-	`sha256:be978697b103a5510665f41ccd5a573d7d49b6e7bc9cb397e03f3d1d8f0345dd`  
		Last Modified: Wed, 27 May 2026 01:58:57 GMT  
		Size: 53.5 MB (53457827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c26675ec1f3692d9d0ae40cb16437ca5b06489ba2f9b8ea466448fb3b6914c`  
		Last Modified: Tue, 09 Jun 2026 21:13:28 GMT  
		Size: 104.7 MB (104707959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:27791443ca70d3559c5f72cee8191f8994d2e8817066d3317a379bfc35b4ac7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5208509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6ef2837bebca831ae01de0e0bd196210c4f7d2be2471ac27a3abc6ac48ff021`

```dockerfile
```

-	Layers:
	-	`sha256:8772e206714b5a443f83077877588069c0ad31c5e2e91cf87b96b74d46ee1b01`  
		Last Modified: Tue, 09 Jun 2026 21:13:26 GMT  
		Size: 5.2 MB (5199218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:266b94c7eeb2cc0e05ad3c0889dcad2ccee1f4401ddb475f014a2025438d5d76`  
		Last Modified: Tue, 09 Jun 2026 21:13:25 GMT  
		Size: 9.3 KB (9291 bytes)  
		MIME: application/vnd.in-toto+json
