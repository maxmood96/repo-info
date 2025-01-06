## `amazoncorretto:8u432-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:3f9158c05ffb5cfa1fa4ac7be38900c4d737ef71f6386005ba6fa4fd4fa24086
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u432-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:372a236b591dac4cffedcc8e4513278134b71ee72fa0d4e6603ded4f6b3bb65f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.9 MB (179925202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb1eca565f926a5923319650f71cb5d4d037f59fb0d3a32208d797dda4038c06`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=1.8.0_432.b06-1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=1.8.0_432.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:899046e4a240e349763e42464f501b60a1bd429af9f38ccd927d9da2124b98de`  
		Last Modified: Sat, 16 Nov 2024 00:03:31 GMT  
		Size: 62.7 MB (62677439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4119095d54bffc42f26c4551eb2a0241897ab588c9f058f7be12797bd7207a16`  
		Size: 117.2 MB (117247763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u432-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c8affcb75ce4c76b2bdd95b0aaec8850f31952108b4984e466ca3197ba2f141b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7493031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c39dc0c176c2a255c3f40d3164c0eaaeb7e4ac2b3de8d39ed23065d753c0aac4`

```dockerfile
```

-	Layers:
	-	`sha256:e6b879bac16058498991fe05a6d97ef54571a1131a813320397cdc34524eea6e`  
		Last Modified: Fri, 20 Dec 2024 22:30:57 GMT  
		Size: 7.5 MB (7483483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79792013d431d0ab213e1531c091a3660f0c544f21bd57ac9efe3849e4b07b3f`  
		Last Modified: Fri, 20 Dec 2024 22:30:57 GMT  
		Size: 9.5 KB (9548 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u432-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e2dafcdf1eb8a7984e5490ac1e711025b93cc7e61275798820f58ea9d3fde71a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.3 MB (126253741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbccdf77cd112ef9e171ab5d439945b6353e1f0d4e78418dabbdc2b886010adc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=1.8.0_432.b06-1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=1.8.0_432.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:ac443ee34758d1600a5b00a6cdb0786b24d6b89a9b4fb2518f0fdcc1f7353b57`  
		Last Modified: Sat, 16 Nov 2024 00:03:57 GMT  
		Size: 64.6 MB (64581887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0cc0aea6cce0ae7b517b1d6c7252e8084bdfab3d7150b753954de51a79a0b9`  
		Last Modified: Sat, 21 Dec 2024 01:36:21 GMT  
		Size: 61.7 MB (61671854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u432-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c3407749dd7a2bd7bd845cd6ac169eb34f973b36e2c839c70038ab00e3bd4646
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5612431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e816f66ea0f17777425531bd385f5f67663248b8969a2449178ba409e8452a9`

```dockerfile
```

-	Layers:
	-	`sha256:490aa278f8df5e44bb5234f0d3c3a88b30852c52c316be0cf187203f23f9c4fb`  
		Size: 5.6 MB (5602804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c21bd4820106dbcae17c9c6e3f91842c5a10615d5bc22955213abe8e96a2cc30`  
		Last Modified: Sat, 21 Dec 2024 01:36:19 GMT  
		Size: 9.6 KB (9627 bytes)  
		MIME: application/vnd.in-toto+json
