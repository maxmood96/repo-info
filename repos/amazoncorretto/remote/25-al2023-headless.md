## `amazoncorretto:25-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:2b27d6f86d26bfc1a960b59713098e523f498379d04fd9633aad4f542301b085
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d83651c970e876f892e3e2b5a39c4eecd182cf8f0c20b97df799078cd931acfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157571943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62016bf8dda3ce58feeebc39aec8d4154860bd37f0270a94ab59719fcc4fceeb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 14 Nov 2025 01:07:30 GMT
COPY /rootfs/ / # buildkit
# Fri, 14 Nov 2025 01:07:30 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:17:21 GMT
ARG version=25.0.1.9-1
# Fri, 14 Nov 2025 02:17:21 GMT
ARG package_version=1
# Fri, 14 Nov 2025 02:17:21 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 14 Nov 2025 02:17:21 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 02:17:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:b64ab808fd6d460065684b4dcddcfaed550a0161a81a4f24db38100a7cef4ade`  
		Last Modified: Tue, 11 Nov 2025 02:45:03 GMT  
		Size: 54.0 MB (53976715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdcc125fb46c2553b476259b92b53653e4d1c14b39a2213daf04a07a457e0ff2`  
		Last Modified: Fri, 14 Nov 2025 02:18:10 GMT  
		Size: 103.6 MB (103595228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:337b7447f6feef5158f5938d78c251cf85f05aab7b1f092a66d4826170ebc6f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5203812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a209fae109b7974f9d6b522680b391cc0353e5c2138a9c33a7c99a245af5085`

```dockerfile
```

-	Layers:
	-	`sha256:66a13f4d3d24c6eb7aaa011836943447d2c76635c8891b7079308cfba417a52a`  
		Last Modified: Fri, 14 Nov 2025 04:51:10 GMT  
		Size: 5.2 MB (5194783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85b73a3f979e9cf35432cd3716a0554f52f494572c42af6415eba90b1e9d7af6`  
		Last Modified: Fri, 14 Nov 2025 04:51:11 GMT  
		Size: 9.0 KB (9029 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:936629110f711d95eb600d074ae4a8675a391897fc50d2fe29ee20acf69cd63d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155413944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:becc7edc499d3c3321b344edc03a9385ccbdbfb23f1ff6e83ff5d1e4673d0598`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 14 Nov 2025 01:25:24 GMT
COPY /rootfs/ / # buildkit
# Fri, 14 Nov 2025 01:25:24 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:21:24 GMT
ARG version=25.0.1.9-1
# Fri, 14 Nov 2025 02:21:24 GMT
ARG package_version=1
# Fri, 14 Nov 2025 02:21:24 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 14 Nov 2025 02:21:24 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 02:21:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:7bff4bcb213fec2224ece2638c720fadc39b0d185d5cfe08391265c58685a0ae`  
		Last Modified: Tue, 11 Nov 2025 02:45:05 GMT  
		Size: 52.9 MB (52876656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656f3891ed57157129402c69f6a00fd27382914ae43f21818065a90c18666f04`  
		Last Modified: Fri, 14 Nov 2025 02:21:59 GMT  
		Size: 102.5 MB (102537288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f242dbdd5b507a15d7bcaa4a844e9ce31c14b3cadb324405ac2b10eeee604e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5202715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1b702f68f3ecea9c91a4c2d0b10d96bf4ed1597d2dec2ef3996ad169c207571`

```dockerfile
```

-	Layers:
	-	`sha256:7f07f1ba497cf915a88b0e43850aac584a19a366e64d939465e5111278ce24c4`  
		Last Modified: Fri, 14 Nov 2025 04:51:15 GMT  
		Size: 5.2 MB (5193594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54464f5e2fe58c7a85148cfc6116012db099868dbdc49d3ca640e1e1415a9ecf`  
		Last Modified: Fri, 14 Nov 2025 04:51:16 GMT  
		Size: 9.1 KB (9121 bytes)  
		MIME: application/vnd.in-toto+json
