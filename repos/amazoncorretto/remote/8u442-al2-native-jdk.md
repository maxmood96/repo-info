## `amazoncorretto:8u442-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:d741293bdb9912b81a93fd9b21477dc7daf081a7cebde9df1da471ddf86ff218
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u442-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:932648ce6f91e7198cc5437bbc011ea8da772b485bd747178e370ed9b60ee3b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (188030230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdc0f01470b2fcfd6a9ab264153f1a880e18516368ba366666b1181872f86780`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=1.8.0_442.b06-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=1.8.0_442.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:f3dc83dc2e4e000fd189efee126db80e38a079b47b8e5229a794a0a6148bfec6`  
		Last Modified: Sat, 08 Mar 2025 04:13:59 GMT  
		Size: 62.8 MB (62772838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfeda5cb5c246f1c7d89475945ca8cf02cd1f9b22d025e77b8d153fe32a96f6c`  
		Last Modified: Thu, 13 Mar 2025 22:53:28 GMT  
		Size: 125.3 MB (125257392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u442-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:978574d4724d76d9d034f22323f2e1476bef4f8b30bb3ec1ccf23cec88e72417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7966109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b6fab5f9c2471835abff03513506900d178c2a964e22092104f1679b290473`

```dockerfile
```

-	Layers:
	-	`sha256:e3e875f4a1f7c1cef81c5cff58c3de7ddf2d5dc84dd454ba4fc57e4a567274fb`  
		Last Modified: Thu, 13 Mar 2025 22:53:25 GMT  
		Size: 8.0 MB (7956516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:498ae4d35a5e380222644559f2f0f4a8affcbc4c4b214ed0464790a3e1b12450`  
		Last Modified: Thu, 13 Mar 2025 22:53:24 GMT  
		Size: 9.6 KB (9593 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u442-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f479138406ff1337328cc46b2d1902a47dbdafbac462ae9af5eec8c0fbccdbc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132130426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa1cbfc71d8037588d339adb64abbdb758b069aab243f553d2c68ae4963d3290`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=1.8.0_442.b06-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=1.8.0_442.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:37d03ccf62e80c78860df81fce0c2ae4e2349efe1a11714ff404080836c55d45`  
		Last Modified: Mon, 10 Mar 2025 14:33:01 GMT  
		Size: 64.6 MB (64576854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b632a3afae3ecb4d09980738e299670f69b41bbb7b617d80f0ee6ff8aba9ace9`  
		Last Modified: Fri, 14 Mar 2025 02:31:13 GMT  
		Size: 67.6 MB (67553572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u442-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e200ba16a5818c65a191d1c9d99a3c4396e120cf30a32d8453d1a3eadcf4eda3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6076351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a7402a630739e0dac4ed0709d69ae1b69aab6c924d30d394cb4514eb231b1aa`

```dockerfile
```

-	Layers:
	-	`sha256:07b6fa715089528cbe8800f9537daa74f3bd5bcfd4b51754ac8d391f3342eb7b`  
		Last Modified: Fri, 14 Mar 2025 02:31:11 GMT  
		Size: 6.1 MB (6066679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d1526e376555002bdcb1ade9e1087058a99af8a68a90bae5b5785955a507b48`  
		Last Modified: Fri, 14 Mar 2025 02:31:10 GMT  
		Size: 9.7 KB (9672 bytes)  
		MIME: application/vnd.in-toto+json
