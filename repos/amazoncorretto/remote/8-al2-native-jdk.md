## `amazoncorretto:8-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:f52dea0bce07b46e53d5adbd8c966cf310496e81f354e86b917d0cbcf0f801f1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2b95a47092157fdd7e441e4e771004d53d86264bf4b5f675114aa8b86c2c1148
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.3 MB (188310992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38163348c7555ce69b62c180d8834edcb14cac94f5b1676fe0b80c161537eb80`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 30 May 2026 00:27:01 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:27:01 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:11:13 GMT
ARG version=1.8.0_492.b09-2
# Sat, 30 May 2026 01:11:13 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH} -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Sat, 30 May 2026 01:11:13 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:11:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:1b617831d6b1041202bed08e227be201a09f5bbe282304143d3ba1e6b9b6cd1e`  
		Last Modified: Wed, 27 May 2026 11:49:15 GMT  
		Size: 62.9 MB (62941950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482b3e1e46d55adf75cb03437ba3f541c32be0b1b74bff89abd30c60eba5ed7a`  
		Last Modified: Sat, 30 May 2026 01:11:38 GMT  
		Size: 125.4 MB (125369042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:00c77e3a775419bec763865d976d7ad61aec0a7dfb86fdf5fae3c330f4551d51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae7d50d3b71a0af6e41bc07799d9dd8db86790fae4cc64da4d81be4f3797390e`

```dockerfile
```

-	Layers:
	-	`sha256:9e8e8fa681a55ec879009445b20260512851ca70b793f8db74bd799a2ee1dc3f`  
		Last Modified: Sat, 30 May 2026 01:11:36 GMT  
		Size: 8.0 MB (7977515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24059856033051d5946fbfb2d5c9ea2ab7b9760b80d76b33bde42586a8bbe12b`  
		Last Modified: Sat, 30 May 2026 01:11:35 GMT  
		Size: 9.7 KB (9711 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6f3c5d440a4cb4e6d216711f0758ab237a18320963d056f99ab8365ccee0f4c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132469396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8920d49ced91bd01cbd09829c826bf8bacc3fa55d7853cfd71551458526ef09`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 30 May 2026 00:29:01 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:29:01 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:11:10 GMT
ARG version=1.8.0_492.b09-2
# Sat, 30 May 2026 01:11:10 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH} -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Sat, 30 May 2026 01:11:10 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:11:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:592be6a6d0447cc7e4d0cd5d164508693821dd45a5dbe90f47689441f936d50c`  
		Last Modified: Thu, 28 May 2026 09:28:16 GMT  
		Size: 64.8 MB (64790709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:935dbe76db373050527e3e6c500743bba8df766f9278b2b1c66f31b7ddaffa11`  
		Last Modified: Sat, 30 May 2026 01:11:27 GMT  
		Size: 67.7 MB (67678687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:25fde6698fc7a072f154e3d94c11beeb9f8d5acf7971c68eb3167c85162a0c72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6092828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c7cec343f78c6f7aec362f62cbdb4dc5314ad79028654f3639019a4acf718fe`

```dockerfile
```

-	Layers:
	-	`sha256:2eaff6f5de6a9a7531e6b37086393a72fcba947c213b460ca88384bcd45ecedd`  
		Last Modified: Sat, 30 May 2026 01:11:25 GMT  
		Size: 6.1 MB (6083038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc35ad11c03cf86df23303c96d8b4a654fee4e4a0ef05c12a93729a24df708a7`  
		Last Modified: Sat, 30 May 2026 01:11:24 GMT  
		Size: 9.8 KB (9790 bytes)  
		MIME: application/vnd.in-toto+json
