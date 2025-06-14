## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:fb32f844d6d73a30e8b51779678069f45ed849abdf49543a9d07069f52fb4e52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:214fcc407142738c633a8978476095446dcba608ae01adbce6f0ee223cbf822c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.3 MB (143312184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c74db6602faace5819c7050deb23a6b07d3928aa97c2511bbc15fda25d909819`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=21.0.7.6-1
# Fri, 09 May 2025 18:18:04 GMT
ARG package_version=1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=21.0.7.6-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:b32084d69388d1a83137a801da01717a35f31eef39012331796a50e2c2385667`  
		Last Modified: Wed, 11 Jun 2025 22:05:56 GMT  
		Size: 53.6 MB (53570360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc45ad609f2bfb26773fb5626a427b1c9287fb31c33e3c929ec7f18cbd9e6c6d`  
		Last Modified: Fri, 13 Jun 2025 17:04:03 GMT  
		Size: 89.7 MB (89741824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4cc872e353f49cce060e43e57d0aca22896941c66e1f228f98bbb91ec2d53941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5219491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f01b6f83bd6de2b1ae51f135e83e0ddbfde38f0b74ff2f07fa69328ff13b6e2`

```dockerfile
```

-	Layers:
	-	`sha256:3e62a7b5fed6ef1479202507dc4ea83462a1a2920e886ad018924cc0a5b2b1c8`  
		Last Modified: Fri, 13 Jun 2025 18:48:56 GMT  
		Size: 5.2 MB (5210564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ead267f2a84f708e15663a00a18a9066005b02982ef93243677e80c3a5e3a4a2`  
		Last Modified: Fri, 13 Jun 2025 18:48:56 GMT  
		Size: 8.9 KB (8927 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:75e32fe1df6f8d7d908ff89657420bc6cda21830faf3d43976f2481f7b5c99d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141369128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebb96dddde2fc271a1be2f3b0b614320d07f105924e415032f7c043c71fb781d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=21.0.7.6-1
# Fri, 09 May 2025 18:18:04 GMT
ARG package_version=1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=21.0.7.6-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:2913b957e7cca1539a6d274307081564a7142eae485bcd51683bbef9106592aa`  
		Last Modified: Thu, 12 Jun 2025 03:47:32 GMT  
		Size: 52.5 MB (52481692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d19ee85c94d6688aac198af35025327b137b28bd14f0692fa96a4172fb569f`  
		Last Modified: Sat, 14 Jun 2025 00:07:52 GMT  
		Size: 88.9 MB (88887436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:610b4eae75d8c45b65342f7d3b51c92937c4c025e01b48c5b1ff4af0478315bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5218363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bad48153a0bbdb16d56f7100a3438b34224e2c1f6ac0bac9c56bc5d628fef7e`

```dockerfile
```

-	Layers:
	-	`sha256:dbf1bed4ff7ecc28cc3f380bb112b279c4cee810c73a66b8d889fb7c73483b5c`  
		Last Modified: Fri, 13 Jun 2025 21:48:56 GMT  
		Size: 5.2 MB (5209357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b793c501bc565dcb68a73656a80c0ca0dc23a8cb76c56690f2f1704a9f20a874`  
		Last Modified: Fri, 13 Jun 2025 21:48:57 GMT  
		Size: 9.0 KB (9006 bytes)  
		MIME: application/vnd.in-toto+json
