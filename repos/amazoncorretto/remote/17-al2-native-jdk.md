## `amazoncorretto:17-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:745403922e7c036fa596a7cb8351f45fdab0e372c80f563cc453473785d36c82
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9ee76930565293064bc0ce735e6ace42dc792435fda83b8ea6802cf6b3d0cede
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228683002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0c057ebe4044a1d03dd677c68161cf58811d9be0afb99740db91e1ff22003a3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Oct 2025 20:18:37 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Oct 2025 20:18:37 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=17.0.17.10-1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:91f0f90aeef889cedc2e056e6976319ec5d96df70bf35b1d46092d2c1f375f2b`  
		Last Modified: Sat, 04 Oct 2025 04:29:16 GMT  
		Size: 62.9 MB (62940620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f6c8987bf0f0fc62dbfd5264b9b1616d9a9dd979ffe063aff7de54889b41e7`  
		Last Modified: Wed, 22 Oct 2025 00:56:03 GMT  
		Size: 165.7 MB (165742382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:eb40b2dae0b017f52883b097c58844e6c633a259fbe56035b61f1d70fd89e8f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5981782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dc6ef9a2e37bf66914aa74246459b9e3c8e2f4d7a9b935a33fa49eece4ae3e0`

```dockerfile
```

-	Layers:
	-	`sha256:42d80ecd53b3258c004b1eb17bb6a2aa95065c39f6ae5717e483a437bc8539e2`  
		Last Modified: Wed, 22 Oct 2025 00:49:48 GMT  
		Size: 6.0 MB (5971820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ee0f3365635dfb2fe05d89ccdb8ddd7a44fc7c9689e73d7681ffe3a720ae3c3`  
		Last Modified: Wed, 22 Oct 2025 00:49:49 GMT  
		Size: 10.0 KB (9962 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:cd26f4608176667c8ab645bda572f5e51846fdf18f95a2d0340a71dae403228c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.1 MB (221066033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a955ac56368b244898e355b8fd9e7ca95264a6e4e21f8fbf46a0918330d85b4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Oct 2025 20:18:41 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Oct 2025 20:18:41 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=17.0.17.10-1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:8b6c0dce7361457a1cee4518c5dc9c75ff3fa343c4460bdb254d7bd18bc1bf03`  
		Last Modified: Sat, 04 Oct 2025 18:25:08 GMT  
		Size: 64.8 MB (64793208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31cba88f1a890177b8e628ccc0eb551ee120e8dfa0866ea45538cec64ef7b80c`  
		Last Modified: Wed, 22 Oct 2025 05:22:44 GMT  
		Size: 156.3 MB (156272825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6286e4c33205b46c7777cc1ec158182a76016d5850d0b44fd7d012d4d2bb621e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5773732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c08fd43cf733b425b373e355924b1aa94646c0b1c7b31f8776daa9e7c282185`

```dockerfile
```

-	Layers:
	-	`sha256:64401f15c7b3455bcb00e0f6810c6dacdac52b97c0ee2c310f807ee6657c37e4`  
		Last Modified: Wed, 22 Oct 2025 00:49:54 GMT  
		Size: 5.8 MB (5763690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fafcd1050a705532b0dd92bcc8400b99898a67b18a390bfda0ca81514f44a84`  
		Last Modified: Wed, 22 Oct 2025 00:49:55 GMT  
		Size: 10.0 KB (10042 bytes)  
		MIME: application/vnd.in-toto+json
