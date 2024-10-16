## `amazoncorretto:8u432-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:7b7b9d947bb8400181f09da75bf182530564f689b280e5d2fb7eec5612d51fa8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u432-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7113e02abf73af37855bcaa9612eef4fdad7dfc166234c8ee3e014e0fd9e427e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.8 MB (171778761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:041e80b00762198798c2095815901af15e6f4c63a7a4cd03b4672b61fea6d45d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 02 Oct 2024 22:07:55 GMT
COPY /rootfs/ / # buildkit
# Wed, 02 Oct 2024 22:07:55 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=1.8.0_432.b06-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=1.8.0_432.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:f956a2176a592b2f85941102c85f1a745c5e74f263c66fc5212bf9eb619f28e1`  
		Last Modified: Thu, 03 Oct 2024 13:25:55 GMT  
		Size: 62.7 MB (62678156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b689bd1323825138596ef1267429d6466c15a4aa7720be7f0e7bfc4dfb1bad`  
		Last Modified: Wed, 16 Oct 2024 17:56:31 GMT  
		Size: 109.1 MB (109100605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u432-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b21c33a021e91e0c31862e2a0f9388b98c3781f429eab350d98c1bc2b572d1e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7507308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b415f0251b7990fa8315f793d7a824195af4b464c04f71c3c53303427957ff5`

```dockerfile
```

-	Layers:
	-	`sha256:593621dde729226c9e7c320f2b44775c33fda86d07defcef99bd968228442654`  
		Last Modified: Wed, 16 Oct 2024 17:56:30 GMT  
		Size: 7.5 MB (7497757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89f55222c29dec804e9f51ec1d48688839f5179a3cb6a300d47cb7b1bc5c52fe`  
		Last Modified: Wed, 16 Oct 2024 17:56:29 GMT  
		Size: 9.6 KB (9551 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u432-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:323a18f1dba0ca2d4a9cd74c4dface3379b9b3c695ea8c85d6a62d445f131ae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117541793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:879558c548cfd6ee857ea2002c29b2bd0488643a23dce82ce0ac6712dd90e2e8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 02 Oct 2024 22:07:59 GMT
COPY /rootfs/ / # buildkit
# Wed, 02 Oct 2024 22:07:59 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=1.8.0_432.b06-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=1.8.0_432.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:17d30073c92a41fbc086cf7be6bbf70600b21ad41c671459f9fd5c536e5182dc`  
		Last Modified: Thu, 03 Oct 2024 13:26:09 GMT  
		Size: 64.6 MB (64592659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad24f7255a22190fe483bda9324d317df0cafdf30d829be7dcefcf6a090b5c28`  
		Last Modified: Wed, 16 Oct 2024 18:05:51 GMT  
		Size: 52.9 MB (52949134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u432-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6a1e23c1a4cfe73e6f7120a25c23da96e8338a8349f5a5949dff365dc90a97d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5623108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:256fcc0599f49f71691d7b20cca3b9e14a4f16ae63c98dad4c35c4804a0e1330`

```dockerfile
```

-	Layers:
	-	`sha256:ac188f9ad6ebc5206c249480a64a54cacd82a5efd7c89cb5040f7cb42b50adcb`  
		Last Modified: Wed, 16 Oct 2024 18:05:50 GMT  
		Size: 5.6 MB (5613477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d73c311c3ab7475371024c491452b0958cc0fa93447743533130c15d02770e25`  
		Last Modified: Wed, 16 Oct 2024 18:05:49 GMT  
		Size: 9.6 KB (9631 bytes)  
		MIME: application/vnd.in-toto+json
