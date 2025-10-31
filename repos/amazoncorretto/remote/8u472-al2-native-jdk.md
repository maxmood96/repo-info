## `amazoncorretto:8u472-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:e10cf1c3a6093bfe34e1576644c22b0f0bd8b921de92e361ebaeb5a79f9183c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u472-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6dc58116c34f6f17585c3aa444c2f8a6028aef77fd29b5a0259c471fe55178c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.2 MB (188173528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf14c90a8b85f506331ea9abc2cc41d895ee900f88b43efe82195f8e88a3ddf3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:45 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:11:33 GMT
ARG version=1.8.0_472.b08-1
# Fri, 31 Oct 2025 00:11:33 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 31 Oct 2025 00:11:33 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:11:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:2e3ea9592aad33f5f11ca8c65604905de30de68b0c38dfad7dee51b605c2a2c5`  
		Last Modified: Thu, 30 Oct 2025 03:52:34 GMT  
		Size: 62.9 MB (62934068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82adf4022e0dd3ec24d202a0017b1e176ef076120de712295b8086176344107`  
		Last Modified: Fri, 31 Oct 2025 00:12:22 GMT  
		Size: 125.2 MB (125239460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u472-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f44fd53fa2e955d7c04237e5255335348bcbcb176e87e994f0674411d8930442
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7986964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4864da73c9d49402b44c18b26b797142fbb3fb0e1d2691fc5369ba6423fa245`

```dockerfile
```

-	Layers:
	-	`sha256:e86c3584a55e6301bcd8db480df4fdb3397ce1a9f5ee662c156afdc5dadd979e`  
		Last Modified: Fri, 31 Oct 2025 03:41:42 GMT  
		Size: 8.0 MB (7977414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64b80c32ef9e547c491956b12f083699f73f38ba92a56b2d33a6efc0794e0171`  
		Last Modified: Fri, 31 Oct 2025 03:41:41 GMT  
		Size: 9.6 KB (9550 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u472-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6d92cb325cedf9da51e2a6d2d66d8f9730fc0a26ee5374cb8f58956837b46945
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132357727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:972eee39e55107b02ad53b23a672de34ceff31cb84f30a8fd415bd5a40c2428a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Oct 2025 23:14:47 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:14:47 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:11:52 GMT
ARG version=1.8.0_472.b08-1
# Fri, 31 Oct 2025 00:11:52 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 31 Oct 2025 00:11:52 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:11:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:2875a69d1768080ef2331610c2aea8f8cfff54b5df360eb9feb01240a7526ff5`  
		Last Modified: Thu, 30 Oct 2025 23:15:16 GMT  
		Size: 64.8 MB (64793458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed704397d28b9ebf9415b6939d853c621199e12a3652c674b2176f39460de92a`  
		Last Modified: Fri, 31 Oct 2025 00:12:30 GMT  
		Size: 67.6 MB (67564269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u472-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:12a9b962375fc4918544c74893f37a7031118101cdc73052a1a070b404dc5da9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6092566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6b96b5ff56c9b45e735cbc2b55194cccd855e0ba5c84d43afed0332cc1c390b`

```dockerfile
```

-	Layers:
	-	`sha256:a06565cef65dcedf1094cc8b9a95b5ca5c89373819cbed50b0f08866884a2682`  
		Last Modified: Fri, 31 Oct 2025 03:51:52 GMT  
		Size: 6.1 MB (6082937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b540e207aeea7daee9f03b272f94bb985c3591b1d42b447c3f5d360a19527cbb`  
		Last Modified: Fri, 31 Oct 2025 03:51:53 GMT  
		Size: 9.6 KB (9629 bytes)  
		MIME: application/vnd.in-toto+json
