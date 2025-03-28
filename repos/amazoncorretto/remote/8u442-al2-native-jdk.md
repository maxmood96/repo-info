## `amazoncorretto:8u442-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:42a17d67f10ea01b2bfceffb69611c7038f07c3f0d7d3ad6ea1327a172d9c7e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u442-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:cd598fc58ad314fa1bb864e04002f903079a60db7b5c7dd50bd7e32d0063c1e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (187980172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae96230007a1a0b449c2ca51e908aa5f66b157b48da3fc4847e7c821a062ab9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=1.8.0_442.b06-1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=1.8.0_442.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:68b5eef1eb563a36e20df422ee1592c70689019fdd12cc4fdc4e4b24c31c1c77`  
		Last Modified: Thu, 27 Mar 2025 19:19:22 GMT  
		Size: 62.8 MB (62752889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc805ee2c52588ca043d2ff7aca4703f12dcd78c733e67f94395135045da4371`  
		Last Modified: Thu, 27 Mar 2025 23:59:01 GMT  
		Size: 125.2 MB (125227283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u442-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:deea96c777ec3804c279bc226f40c1e98944c3b1a4d49fe4ed4f4e023eb3b68e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7966109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cc1868b702ecd4cdc8c96399a2b53ce769cb25e8ed1f0365993fc0a36f10c52`

```dockerfile
```

-	Layers:
	-	`sha256:af08766028091cd46e434f47f5b30c1709fc39ffb4f441137bc4d67f4a8ac0e4`  
		Last Modified: Thu, 27 Mar 2025 23:58:58 GMT  
		Size: 8.0 MB (7956516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:563712078d3bf20ecf8e9479afa2b92a07dad65696c8e06da50e8bde8fad0e94`  
		Last Modified: Thu, 27 Mar 2025 23:58:57 GMT  
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
