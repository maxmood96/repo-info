## `amazoncorretto:22-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:77407cf7eaaaf7267bc100fa55df920206ad662d71d34dbb0d69dd2efff4d74a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:22-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3d6db0b30ae5b793746d8644e0c691c10d9bc1c767b0816f031e397b9016e9c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.7 MB (140658763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fd82c5822c4b2afa495878a0b42e4a00eec436ece969b6adb6d63b24c325412`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Jul 2024 21:19:33 GMT
COPY dir:8edd892881e79c0c11996c1a60e2c04d066537e06bdf88e1def994a6148ea23c in / 
# Thu, 11 Jul 2024 21:19:33 GMT
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
	-	`sha256:ee5ee70789863a32f444d11d47a2849acfc6089e3e8c78d196f63475ee994293`  
		Last Modified: Thu, 11 Jul 2024 21:19:58 GMT  
		Size: 52.3 MB (52313695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fddf26c240eb16a85f89b762ab5d17db44456a330d4e6bea9e8f3b6eeb9d07a`  
		Last Modified: Thu, 18 Jul 2024 00:56:25 GMT  
		Size: 88.3 MB (88345068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:54f5c13fa72d15f1aef0dd9207626b78b4e9863b2420fc86da414e7179023911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5194943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa5d3ae8569604a42e08e986cb68f564833847f146eed1ee350b871c2b5e2b51`

```dockerfile
```

-	Layers:
	-	`sha256:1ac6b4bc88990ead942c99efb261c0d076939955d95378d7723decea9d5b1271`  
		Last Modified: Thu, 18 Jul 2024 00:56:22 GMT  
		Size: 5.2 MB (5186101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c8640b6933720c6be82f616cbd5e0434837beb6c536726a69e0d7bbd32daa64`  
		Last Modified: Thu, 18 Jul 2024 00:56:22 GMT  
		Size: 8.8 KB (8842 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:22-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:2739240428474563f7c7401334f1c0e6c88fc329f84243f9c3f55f5c9c339bbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 MB (138705640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c662835727ff750b49979cdeb98fa3f30221090f55561b5d93aa1c1e41fb2d4`
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
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
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
	-	`sha256:522d6fa6cb69d823eeaf813fe2b11d3998e530030b5d73a933c6fe0263a897a7`  
		Last Modified: Thu, 18 Jul 2024 01:27:06 GMT  
		Size: 87.3 MB (87304502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7dd9f113f5edcfe48c68dfb13f3c639ae89fb4c25f30ad9ba07766ab86bf5e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5193220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31f1a5eac9af822dd89e2af367b7e7858a12a3881af6f433d999ceabf98bb5a3`

```dockerfile
```

-	Layers:
	-	`sha256:f86fd93742928a880bc725dfe3f9c736c0c10aa05fc01182e40f6973b878201c`  
		Last Modified: Thu, 18 Jul 2024 01:27:04 GMT  
		Size: 5.2 MB (5184085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0268fb19a209d5bcbb0a7d0d181d3e39ddb6295c169a81f0a66515d7966d008`  
		Last Modified: Thu, 18 Jul 2024 01:27:03 GMT  
		Size: 9.1 KB (9135 bytes)  
		MIME: application/vnd.in-toto+json
