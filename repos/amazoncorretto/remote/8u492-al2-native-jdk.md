## `amazoncorretto:8u492-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:a9877d7817c584b47427baefb4136e06adbad41934b146a51d56cf3bdb49808a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u492-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8036e0cc914dd88c34fc75a1502859b210160a3553e81abb9bdeaa1822e587a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.3 MB (188321038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f5e1108619e5c8a2f3ad4b17cf77e4259a682c588fa5969969bdfa7ccb5bb9a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:21 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:21 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 21:32:54 GMT
ARG version=1.8.0_492.b09-1
# Wed, 22 Apr 2026 21:32:54 GMT
# ARGS: version=1.8.0_492.b09-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH} -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 22 Apr 2026 21:32:54 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:32:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:5a3a1a219789b0285ea1d6a41ad03e6fab76f369592968c458dbfffd408719dd`  
		Last Modified: Thu, 09 Apr 2026 08:25:08 GMT  
		Size: 63.0 MB (62955266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d050ed7807ad08ad29b743cb34db004d662c96ade66f2371e308528e214eefc4`  
		Last Modified: Wed, 22 Apr 2026 21:33:17 GMT  
		Size: 125.4 MB (125365772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u492-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fffc1d1c35b0c8ae9a521130430ae910438a51ef3a8ff44931c2153352f782bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:571bb0192b3aa4e8aa2c9d0ea048c412ed423e63c7bf1aa360c9147caf96cc97`

```dockerfile
```

-	Layers:
	-	`sha256:69040f5d533d6428db5ccd72c291ba0ddd442f6c8bf35f4ad1ddb186d11b60f7`  
		Last Modified: Wed, 22 Apr 2026 21:33:14 GMT  
		Size: 8.0 MB (7977515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdc6ad87aaa89763e696392480d7fc89fa6192fcabe5e47eefc12e300d7bca6b`  
		Last Modified: Wed, 22 Apr 2026 21:33:14 GMT  
		Size: 9.7 KB (9711 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u492-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:bf770a526600e4063a262c36a9ba3d7c1263838a82849ce526cb11df616075f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132500769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b42da4ae3b02bd1b17e3cbd730fc6c7f79af5b8d4d2992939e92593c679afcf0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:35 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:35 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 21:32:48 GMT
ARG version=1.8.0_492.b09-1
# Wed, 22 Apr 2026 21:32:48 GMT
# ARGS: version=1.8.0_492.b09-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH} -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 22 Apr 2026 21:32:48 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:32:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:f1f2697b3535de3cb27d338e724d6283baf064a258669349257ede7e5670fff3`  
		Last Modified: Thu, 09 Apr 2026 08:25:15 GMT  
		Size: 64.8 MB (64802975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:372f25895d743f576f37dfa0b1e350269ade4c2bf6637cb8b42d71e4227b114c`  
		Last Modified: Wed, 22 Apr 2026 21:33:04 GMT  
		Size: 67.7 MB (67697794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u492-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4355249c60739788ee61087dd0ef45a250e0337d5c8ecc41cab642d47ab26e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6092828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06b7f35777371c91ae2f166f3816102a04c468d2a907ced5e4e1e90ee5123fdf`

```dockerfile
```

-	Layers:
	-	`sha256:3bb69450e9f23d1a957db0b7f4ae5f47320f6ebe9d44762c2097fb98afd43675`  
		Last Modified: Wed, 22 Apr 2026 21:33:03 GMT  
		Size: 6.1 MB (6083038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4877c16337ae991f1ea7649ab81db1ad3de676c825a7498ae82f1fb2c695be42`  
		Last Modified: Wed, 22 Apr 2026 21:33:02 GMT  
		Size: 9.8 KB (9790 bytes)  
		MIME: application/vnd.in-toto+json
