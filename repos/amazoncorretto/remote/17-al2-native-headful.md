## `amazoncorretto:17-al2-native-headful`

```console
$ docker pull amazoncorretto@sha256:c3c3f7162405e453ec1917bb4a0a0324b3fde385082db7dbe55ea4ecde001a6e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:83e7e4db5ddfde7855b6e32fd39bfc25bffe2d194d6dade8b9ce13bdc3fac7bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.1 MB (154148161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5299902efac26b4a97689062424168d812a4dd681387e82ed26ae4cf889a599`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:7f8efc14a219454ff8f309d236d31a55327a6ff05dda42df51689619d9a34fdc`  
		Last Modified: Fri, 06 Sep 2024 18:59:36 GMT  
		Size: 62.7 MB (62695547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53aaa705dedd1ed4a4c32df1f021b2e8b75b2399127b79a0063ef36cfea8a79e`  
		Last Modified: Sat, 07 Sep 2024 01:06:10 GMT  
		Size: 91.5 MB (91452614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:64e40c7ef37d05f3c8f9ba74061cfe921a9016a45a9ed68b5335a662955b7ca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5869512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88aa572ff21ad77a9b8a07a73a9b0fe173ca8ab301f276973dbed25822125f77`

```dockerfile
```

-	Layers:
	-	`sha256:40d26a1a68782c561a27e0fd947d671a540d89f81f78197ae7488f2597a7426c`  
		Last Modified: Sat, 07 Sep 2024 01:06:07 GMT  
		Size: 5.9 MB (5860075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5c41c855bed2d14d3de458a0922d8a68b87abdee21fc6413336d070f11f4483`  
		Last Modified: Sat, 07 Sep 2024 01:06:07 GMT  
		Size: 9.4 KB (9437 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:83f704b72662cc3a372cfd9a72d8950ea221e99bf45eb596f629c6297bfbb855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.8 MB (146778571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a32973dbbfdda03928cfe6c1ec07756df3e093a7d8f63aaff8d58e800c198e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:0f0968c920788bb8a898446e0bbe8ea6b11fcbf7f55810ef51044775a045d6c9`  
		Last Modified: Fri, 06 Sep 2024 18:59:50 GMT  
		Size: 64.6 MB (64586343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6332125943a818eb77dfa6109d3298b5f88a2130e5d036442eef4be2607adbab`  
		Last Modified: Sat, 07 Sep 2024 13:23:08 GMT  
		Size: 82.2 MB (82192228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:715bec05885a7b3fb05f7e95cc5360c7ef5eab2a5ee9106f922e8c48689d12ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5661275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:391bf22e5a7c303179ccc9991901329d0dbc2cfa033ba5d4ad5f68a25de55b15`

```dockerfile
```

-	Layers:
	-	`sha256:31563539fdb33a17a29ebba7da87e7957248c9443f7e13ddcd74c1bfd28711f0`  
		Last Modified: Sat, 07 Sep 2024 13:23:06 GMT  
		Size: 5.7 MB (5651477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76936dd8f978100ac471415ac3dd12abc780c4365367e28b57902d5cc2d33a56`  
		Last Modified: Sat, 07 Sep 2024 13:23:05 GMT  
		Size: 9.8 KB (9798 bytes)  
		MIME: application/vnd.in-toto+json
