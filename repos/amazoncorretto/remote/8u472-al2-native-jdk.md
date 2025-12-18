## `amazoncorretto:8u472-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:8bd0b3faf992e771b3a9710e32389f236f6e85ad2f7b78ccf9fb213e4b3a25f4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u472-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:64c99ca9ccb7991c8f9618faeffe918f4f9c6b418838c9294515cc9493b41e49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.2 MB (188195415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9fa3a702333f7ae2e2a569623e7ec95062c803c97ca26139289196cf476dd8d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:55 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:55 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 01:17:42 GMT
ARG version=1.8.0_472.b08-1
# Thu, 18 Dec 2025 01:17:42 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 18 Dec 2025 01:17:42 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:17:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:364e8e668f0e62a54627e7d364c5d2a3a16f70f1c962628fd84b9ef8fb667d21`  
		Last Modified: Thu, 11 Dec 2025 05:04:46 GMT  
		Size: 62.9 MB (62940975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc408b9e62625748147275ca19b21dbbe5fd9f9a7404008c607f16351a8b8ce4`  
		Last Modified: Thu, 18 Dec 2025 01:18:38 GMT  
		Size: 125.3 MB (125254440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u472-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a119e3202f7935cf7a604fb92c5b364002f75200f68b8b099e8dc4feef842ec0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7986968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:beef4d86d28f3fbaf581a778dedc3cd6fd981dfe01176774757b580ecd346346`

```dockerfile
```

-	Layers:
	-	`sha256:a2fbeec915de4eaeb38caa08b99345061c6f9eb089df255fe1af2d82b0c43463`  
		Last Modified: Thu, 18 Dec 2025 04:51:52 GMT  
		Size: 8.0 MB (7977418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:251844e005834ac2ff17a8241b0d77365ecc891e3f1b4762e6806edca05a6139`  
		Last Modified: Thu, 18 Dec 2025 04:51:53 GMT  
		Size: 9.6 KB (9550 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u472-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5a190874d011ccc5b29cf5c830910b3f64fd98e5a2fdccfb113d92d1b25dc73b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132360366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58c34dd13ec9f91036ca77076fc1453260e699b12d3d69915260c6f1a22dc4ea`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:41 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:41 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 01:25:25 GMT
ARG version=1.8.0_472.b08-1
# Thu, 18 Dec 2025 01:25:25 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 18 Dec 2025 01:25:25 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:25:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:535c61639a173696e963cd2ada71746467bbf8ddd232fde633f87067e08137f5`  
		Last Modified: Thu, 11 Dec 2025 21:46:54 GMT  
		Size: 64.8 MB (64795755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad95754e2bce5c6c7090de2b6baaa56883f5d191178e3190f569d285d0c62c2`  
		Last Modified: Thu, 18 Dec 2025 01:25:56 GMT  
		Size: 67.6 MB (67564611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u472-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:bcd0531e8a90eb52c53c6fbec51177e0f71c9f3356d31ef5e16fc7d2ec10e089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6092570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c8b98f87fec5ffc1165704314dc5d0306c03c3ae0ecc1d9678371d933c01f0e`

```dockerfile
```

-	Layers:
	-	`sha256:87be62e089e9edd466f38f2be4adc7c0715774910a7d0a47cca3a0c93aefa27c`  
		Last Modified: Thu, 18 Dec 2025 04:51:59 GMT  
		Size: 6.1 MB (6082941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68df05f0101e017a545069f51c410489a7d316d284c2212a0ff6227deabb6790`  
		Last Modified: Thu, 18 Dec 2025 04:52:00 GMT  
		Size: 9.6 KB (9629 bytes)  
		MIME: application/vnd.in-toto+json
