## `amazoncorretto:8u422-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:8f7db4869f1121b0d1a9356f66f4d16a4a4e9b0b77eb9233dcd9515339644875
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u422-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:191389af0bc53fdfb223b0906db85e6c7a196177c06f418eb6a506f6ca8bd1bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187909871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fe5e7a26db1eac1f43b073bcb0dedaa53cb7e22933ba1f0c1ef98854202de95`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Jul 2024 21:23:24 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Jul 2024 21:23:24 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=1.8.0_422.b05-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=1.8.0_422.b05-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:37766f9d8ddf179208313163dc89d8d39dc16ba3be3bc46534855c244565cdd4`  
		Last Modified: Fri, 12 Jul 2024 13:12:20 GMT  
		Size: 62.6 MB (62649406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d227b04d98d71fe6f848f4bb57ab3817c936bc22d26c30fd18c13cd4741d89`  
		Last Modified: Tue, 23 Jul 2024 00:07:48 GMT  
		Size: 125.3 MB (125260465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u422-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:51a42ef9580b74a73ed0b2a82e390722b79cd88edfb632cd2aae1a74fb227367
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7980711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0da904617e2d2dcbda45627ca204bc6f56fd8cab96f4ee69313a0fed71890232`

```dockerfile
```

-	Layers:
	-	`sha256:b4d41b097a40676feff043939dd657a394befdbd13cc07905900b1489671b31e`  
		Last Modified: Tue, 23 Jul 2024 00:07:46 GMT  
		Size: 8.0 MB (7971152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8c3e35519e21795ed0eedebbe1a828f239a5fd5ec8b8152d81ffc90d8e826ce`  
		Last Modified: Tue, 23 Jul 2024 00:07:46 GMT  
		Size: 9.6 KB (9559 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u422-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:709481d1836a51d1376aa188fac8ecccbec2060d1d43519901c19bbcdbfae6a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132128669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbacd96d591953efca717dc14cc3c9c22f7faf14f6c731c8de7656528b9ab830`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY dir:cdeeb89e10fdbe3f38b9e5f6d359ee1afb9caaa1018fdd71fd6c0374dc592a5f in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=1.8.0_422.b05-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=1.8.0_422.b05-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:4ba2ef523fa6e28aa5a068ecb9167a3b9efa29481c3ecc6d34fab1c350b98b6d`  
		Last Modified: Thu, 18 Jul 2024 21:40:02 GMT  
		Size: 64.6 MB (64575311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c55d51d5d88ccd10b6665e6926d0faed7ad5c42d274e1c66595863143b37da11`  
		Last Modified: Thu, 18 Jul 2024 22:51:21 GMT  
		Size: 67.6 MB (67553358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u422-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8bb51c19a8866713576c1a1ecd39c587b56ecc4feea774061bb18897304720cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6087324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42d04adb9f71c4b70bb752b37f212ec1979d2b56c86f3456fc5c5b8f0b263ef7`

```dockerfile
```

-	Layers:
	-	`sha256:09dcc6cd9bae4c49e645576939cf85622b81598add41c94f83012f985483d55c`  
		Last Modified: Thu, 18 Jul 2024 22:51:19 GMT  
		Size: 6.1 MB (6077693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3be4d50f4f36afa7f34931ea6317a9f9c082264ac5abf46662f07f5177b87ec1`  
		Last Modified: Thu, 18 Jul 2024 22:51:19 GMT  
		Size: 9.6 KB (9631 bytes)  
		MIME: application/vnd.in-toto+json
