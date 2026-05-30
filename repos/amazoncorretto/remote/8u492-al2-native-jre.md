## `amazoncorretto:8u492-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:20d080726e1cb71fae00c3e9970992df0cdb295e9c02559d6e88ef1ab794e7f5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u492-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4d4045318b6026060bf594a1036b994814e49ab031332c35db81c13b2ff58775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.1 MB (172097431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a387819dde4eff96a15f3728181f4935496cf4c6788124a22c12f13a9b73b5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 30 May 2026 00:27:01 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:27:01 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:11:04 GMT
ARG version=1.8.0_492.b09-2
# Sat, 30 May 2026 01:11:04 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Sat, 30 May 2026 01:11:04 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:11:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:1b617831d6b1041202bed08e227be201a09f5bbe282304143d3ba1e6b9b6cd1e`  
		Last Modified: Wed, 27 May 2026 11:49:15 GMT  
		Size: 62.9 MB (62941950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7281405df30756684a03bb44b6c18601718fd853632e1666892199483074974`  
		Last Modified: Sat, 30 May 2026 01:11:26 GMT  
		Size: 109.2 MB (109155481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u492-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:185fbbd9a9c08da5c278596fcd4bb0cc968a228b69202c0caaafd0a830102e84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7513903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2582593eaacfa940282f15a33fd5a96ebab9976e16a0c50d343f5314d0ae13c3`

```dockerfile
```

-	Layers:
	-	`sha256:37313f961fdf2a7896c64d4d4202abbdac7e80cd3874b299597a46f67b6989db`  
		Last Modified: Sat, 30 May 2026 01:11:23 GMT  
		Size: 7.5 MB (7504229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa625ddee50d34bea87e0b1033ce146917b81f6a297756d8abe9a26cb9fbe9ba`  
		Last Modified: Sat, 30 May 2026 01:11:23 GMT  
		Size: 9.7 KB (9674 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u492-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d4f11a5c5f64ff1802272e096c0fdd3580b892a80b5fc76dfee50131154acde7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117740439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a779b21449a5e91f7df97b3134b68e2d6fb1a2c7fd2a998b1fda3418fd0eae97`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 30 May 2026 00:29:01 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:29:01 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:10:45 GMT
ARG version=1.8.0_492.b09-2
# Sat, 30 May 2026 01:10:45 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Sat, 30 May 2026 01:10:45 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:10:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:592be6a6d0447cc7e4d0cd5d164508693821dd45a5dbe90f47689441f936d50c`  
		Last Modified: Thu, 28 May 2026 09:28:16 GMT  
		Size: 64.8 MB (64790709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c469a653181e1f0a1f66340e73ba44482b6812c802e0f787906d82244dda8eac`  
		Last Modified: Sat, 30 May 2026 01:10:59 GMT  
		Size: 52.9 MB (52949730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u492-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c55a5998fe9b48ce92d0f50d095b27df6d23ab97acc67ddc4fbdc518a679bbc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5628741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86d167dffdbaa729480f726637cc7d70a417275c8c44046ca72f671895874e2`

```dockerfile
```

-	Layers:
	-	`sha256:57aef8d2f6363b3395850c0877ec6da1834f7c9cc4ff1dee99d2748d9011a789`  
		Last Modified: Sat, 30 May 2026 01:10:58 GMT  
		Size: 5.6 MB (5618988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:308b76475f64c3d948c930785fff7753b983c870c15cc374909f4a0cbe2433c4`  
		Last Modified: Sat, 30 May 2026 01:10:58 GMT  
		Size: 9.8 KB (9753 bytes)  
		MIME: application/vnd.in-toto+json
