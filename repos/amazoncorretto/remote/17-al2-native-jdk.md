## `amazoncorretto:17-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:9ccf9c71012c11c4b233799b7553c240c990378c0fb05f01c21d45c31699c5cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:75839b42b710926e4417bf4659169e149056af8dc705e3e4fe1f7fba5b7b37d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.8 MB (228758984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce80c0247b90f84fe501fdb96dcbd2271a6387d40a31bc50a80e290dcd3e4d1f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 04 May 2026 19:39:12 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:39:12 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:12:46 GMT
ARG version=17.0.19.10-1
# Mon, 04 May 2026 20:12:46 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2.1.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Mon, 04 May 2026 20:12:46 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:12:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:1deb63baef8049d37b87192670264bba74a0207718cc43a1c66077f5bf81a3c8`  
		Last Modified: Sat, 02 May 2026 04:14:38 GMT  
		Size: 62.9 MB (62860009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28cde7cd1e9d1ecdac7aa9bce9a74c71c93cdb6cfa50ca30c63d743f0d35b7ea`  
		Last Modified: Mon, 04 May 2026 20:13:09 GMT  
		Size: 165.9 MB (165898975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:dac532254c5992e7c56eff6c3065a960b10d44405f786114f35ba7006ca51e62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5982800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:773854684aeaf19d3e209011c792775c2e9e4744e425b5acbae1efb3f71031ac`

```dockerfile
```

-	Layers:
	-	`sha256:9a96193cb28df66dd8a00e6a61f4540abe2c47ce24e05fc36113cfd02fc849e5`  
		Last Modified: Mon, 04 May 2026 20:13:05 GMT  
		Size: 6.0 MB (5972740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:53401af06f7e2557ab272f3b3afe70d67e95d9c5b67997ec87a49ebca2994f50`  
		Last Modified: Mon, 04 May 2026 20:13:05 GMT  
		Size: 10.1 KB (10060 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:924b731629fee92a352c3b81e806f78506bd93009bfb27f6cb94528ee2b3a2bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.3 MB (221268834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bdc66a5855692c996a18ff5b6f32bed6ef82fb3363f1d7dd99a556717c3ba98`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 04 May 2026 19:40:38 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:40:38 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:12:30 GMT
ARG version=17.0.19.10-1
# Mon, 04 May 2026 20:12:30 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2.1.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Mon, 04 May 2026 20:12:30 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:12:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:d78bec86efed585192790ef27ca98e5305604b02ec838239205e149e3aff726c`  
		Last Modified: Mon, 04 May 2026 10:12:23 GMT  
		Size: 64.8 MB (64795531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c0ae122283c49e29b784c6e82b6588f08a7e2310c9b16fe9fc497f673a00a6d`  
		Last Modified: Mon, 04 May 2026 20:12:53 GMT  
		Size: 156.5 MB (156473303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3a0946ffef2d7e34c09ff6b178080c422daaf81cdc4f28a6156fff3b7fda30ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5774751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:994c669f9495a46322ac7616f437f58d7b4158a2b622412fc64410b6be157b93`

```dockerfile
```

-	Layers:
	-	`sha256:86fe80ed3dadb743eea682b93bb2e357f639cab9e280839c0795aa9f9558cc5b`  
		Last Modified: Mon, 04 May 2026 20:12:49 GMT  
		Size: 5.8 MB (5764611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e06cc00a46cf5fbe06738463d2923b51d9a1cf1e825d791ed46be49ba9e45455`  
		Last Modified: Mon, 04 May 2026 20:12:49 GMT  
		Size: 10.1 KB (10140 bytes)  
		MIME: application/vnd.in-toto+json
