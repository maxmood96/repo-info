## `amazoncorretto:8-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:78791569fb15a481f99daf83176d39e8d79a9d6425b0613594691e83367db002
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:1f2368336962a184ee08f094c55742c61325d8ccbbceb7f3a045ff9ae2b75e81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.3 MB (188317460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a5ebc325250efa2ab791f339b3bfda79f62407a7cda3eb2e4759e93ca1f315`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jun 2026 00:09:40 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jun 2026 00:09:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 01:14:55 GMT
ARG version=1.8.0_492.b09-2
# Tue, 16 Jun 2026 01:14:55 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH} -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Jun 2026 01:14:55 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 01:14:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:1b617831d6b1041202bed08e227be201a09f5bbe282304143d3ba1e6b9b6cd1e`  
		Last Modified: Wed, 27 May 2026 11:49:15 GMT  
		Size: 62.9 MB (62941950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3c63cadc82dd25ca3feba6d6fde313a54f03d8f44f06036439338ceb27c763`  
		Last Modified: Tue, 16 Jun 2026 01:15:20 GMT  
		Size: 125.4 MB (125375510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c78efcd0149e1362de0755474044ebe910dd611098bb253abebb0464de00124e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf16168f157f703960a25c22624a8838bb4e01da17091de17d41df0b374b4363`

```dockerfile
```

-	Layers:
	-	`sha256:ab66c9d33c73aace6b39cd2c21e08538c76a979f4e05f498b1c499f42febf954`  
		Last Modified: Tue, 16 Jun 2026 01:15:18 GMT  
		Size: 8.0 MB (7977515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32e3ae66b463f27bdfd39de0f39d87fd3b30aa75b77a45029f0476b35cb3f0ee`  
		Last Modified: Tue, 16 Jun 2026 01:15:17 GMT  
		Size: 9.7 KB (9710 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c5af3d03fe71ab489fb62e6076a906ee0c3c5541670a56c37785d7564f70ba9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.5 MB (132469797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1b1ebb00f7212bb12812cbd2ae342ba59c456b75d16092d8b04e631c62bee72`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jun 2026 00:10:52 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jun 2026 00:10:52 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 01:15:49 GMT
ARG version=1.8.0_492.b09-2
# Tue, 16 Jun 2026 01:15:49 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH} -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Jun 2026 01:15:49 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 01:15:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:592be6a6d0447cc7e4d0cd5d164508693821dd45a5dbe90f47689441f936d50c`  
		Last Modified: Thu, 28 May 2026 09:28:16 GMT  
		Size: 64.8 MB (64790709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc7af7c02ab371e9866d2f34c0a5e75acab3bd51621582f7fa6012a5bfa4020`  
		Last Modified: Tue, 16 Jun 2026 01:16:05 GMT  
		Size: 67.7 MB (67679088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b4c28fbcf97e8df39428bbcbe1af32057bafdc61d6e2e57089e9ae417a203ff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6092828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fb02f5286922d1dc88d507ce108e4289a337def0aa13c9b32bcf5f24bec059f`

```dockerfile
```

-	Layers:
	-	`sha256:c8dae81f0a8fcb8f8070f969934f361b2171eed37af8facee9d855ac97e87427`  
		Last Modified: Tue, 16 Jun 2026 01:16:03 GMT  
		Size: 6.1 MB (6083038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a2dba640a9ddb90e998589a7d2033fd72c0ebccdd7e91e4e65b71a4ae9c6ba7`  
		Last Modified: Tue, 16 Jun 2026 01:16:03 GMT  
		Size: 9.8 KB (9790 bytes)  
		MIME: application/vnd.in-toto+json
