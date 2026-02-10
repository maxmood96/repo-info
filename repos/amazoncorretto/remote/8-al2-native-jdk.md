## `amazoncorretto:8-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:b66ecd4c9e4ae8fafa1848a1fc74f7c93f5c51530f98d0154220c81842301812
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:fa8f12321468981538b0dd993fe2637f1b3ee1dce1736a8ace123ccd2bce4481
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.2 MB (188248426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:871f6f4cb6ddd029f1c4c31dfe0364e6d6f169047d05b64e659dc4c3788c8859`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 18:14:13 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:14:13 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 18:31:07 GMT
ARG version=1.8.0_482.b08-1
# Tue, 10 Feb 2026 18:31:07 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 10 Feb 2026 18:31:07 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 18:31:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:f5abe3fbfd395e17e5203e7213ac7dbf150f56cd98e8268563339f7d27569870`  
		Last Modified: Tue, 10 Feb 2026 14:46:03 GMT  
		Size: 63.0 MB (62958957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:495afc70cc9783c05b4acb10ed2e2f6c24a7708ef4671a9f6ec53e389a3d7cda`  
		Last Modified: Tue, 10 Feb 2026 18:31:31 GMT  
		Size: 125.3 MB (125289469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:17df8e32720e421b4b4f40594915ae2deac7e4ebc56fa0a88af0483a1ebe95d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7986968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4412477b4e787c77a713550bdc6a22fd238d65274b83c01d0819d6daf1d94d33`

```dockerfile
```

-	Layers:
	-	`sha256:f2825124e7d4c0280bf49cb74b9a5f113ed96cd628d588b1b8644b5504fe899b`  
		Last Modified: Tue, 10 Feb 2026 18:31:28 GMT  
		Size: 8.0 MB (7977418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67b8637d0af451b5d336db581e8ee678169b4369d290fc346f97d1eee1d6c2e4`  
		Last Modified: Tue, 10 Feb 2026 18:31:28 GMT  
		Size: 9.6 KB (9550 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6bfbcc081a97a4dec96c89749e715d085a570cbe0d861b8ab9a5cf409220d678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.4 MB (132408992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed1d6197e84506cc0b769c263949603d55c3f17e2743f0a674bc79e14c92b4b3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 18:14:03 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:14:03 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 18:30:41 GMT
ARG version=1.8.0_482.b08-1
# Tue, 10 Feb 2026 18:30:41 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 10 Feb 2026 18:30:41 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 18:30:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:7b625f12eaf5f52ff71ffa6d83678b0481194ed88dfaa20ee4b8481abb9ba247`  
		Last Modified: Tue, 10 Feb 2026 18:14:19 GMT  
		Size: 64.8 MB (64799476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb7028ad90c9d5813d0d3d1c6cc38bb500b03f4d8d8b0856c6c4effdc88938c`  
		Last Modified: Tue, 10 Feb 2026 18:30:57 GMT  
		Size: 67.6 MB (67609516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:af88a8d7a84cd4ad71eb1e992a783a7b7b6a2a2387f37c3092a33930238ac93d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6092570 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aadea26e74b995f2d17f2208aac5de0a8b3fdf3c5d6b1f57408d7e25986aad85`

```dockerfile
```

-	Layers:
	-	`sha256:0638b285466880c4294914aa2c2518bb4a095d0428f89aa14449948778b318c7`  
		Last Modified: Tue, 10 Feb 2026 18:30:56 GMT  
		Size: 6.1 MB (6082941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec1461223fb656c672b5dd6107cf743ef8bf5182a0d9d1cb8d97ffe4d3eff59e`  
		Last Modified: Tue, 10 Feb 2026 18:30:55 GMT  
		Size: 9.6 KB (9629 bytes)  
		MIME: application/vnd.in-toto+json
