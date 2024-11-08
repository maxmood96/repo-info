## `amazoncorretto:8u432-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:2cfa4a46a00ff8b9a81b924b7cc9467340360e5071a900be63923008cc0c9c73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u432-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:afd95c3c809c492cb4b4d278dec9cebef1376e10cd841114785044636a189558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.8 MB (171783428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a6647326a16a95ddd20000e36662e7bee90e3865408c89d02a44e13d88746d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
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
	-	`sha256:8430d4c5a00587f0a8dc4c62f82455c123b54b9016d43897ee77c496c018a8bd`  
		Last Modified: Wed, 06 Nov 2024 20:48:04 GMT  
		Size: 62.7 MB (62681042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db0c63f6f9d0b031aba116e76e60b44d70d242750329ce4870d94933eca9903`  
		Last Modified: Thu, 07 Nov 2024 21:48:10 GMT  
		Size: 109.1 MB (109102386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u432-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a2d7bd8b69e566970d6c6e565e1ca303be3c35468540e7a97127b581fb48d5a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7507291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e93fae05c1ad99de110ee9ef10aa7a1d1e2e49e55c3dae4cdea0f6a621ee9691`

```dockerfile
```

-	Layers:
	-	`sha256:b162c472166a764780ded6649dbf52b293bcff3c31f89680827458bb94b8db7c`  
		Last Modified: Thu, 07 Nov 2024 21:48:05 GMT  
		Size: 7.5 MB (7497744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d20dd7fc3881dfbfe05c6dcdff60b3574b21d1112556c22d107245f8cc411040`  
		Last Modified: Thu, 07 Nov 2024 21:48:05 GMT  
		Size: 9.5 KB (9547 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u432-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:4f8796c44afe42fc0ab193f8b86a4ad0daeae2fd654d2a5c694dcc6a74fee769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117529676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36771b7e3bacf8e5e061a0d73b3fa3eb106abbc7f4fb4851594180679d4874ea`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
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
	-	`sha256:0a62aca1c7d7ec3e0e098bf23685d8f0fcd19e33577a91dafc6dd30bef06deca`  
		Last Modified: Wed, 06 Nov 2024 20:48:17 GMT  
		Size: 64.6 MB (64588571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ac15cedd55fa413e7775b1665d2118ddf777695e0e487fe63b8666dab891b0`  
		Last Modified: Thu, 07 Nov 2024 21:49:09 GMT  
		Size: 52.9 MB (52941105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u432-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:abad0505e764fa57a1f30feec0d7b218bc765db4068af70b50c4908d6bb18c2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5623091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:454f8e7715fe3af4243b0c75e5b96cdad2299f35af82e260a8f760123f5878e0`

```dockerfile
```

-	Layers:
	-	`sha256:6625537654dd60a620d6896e61d70a9051b3493e045b5bae9f3adf38c00c4805`  
		Last Modified: Thu, 07 Nov 2024 21:49:08 GMT  
		Size: 5.6 MB (5613464 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8eb96e1465cf2869ad818905f68e16ecb9a622114ab31c892f4e32245d2cc988`  
		Last Modified: Thu, 07 Nov 2024 21:49:07 GMT  
		Size: 9.6 KB (9627 bytes)  
		MIME: application/vnd.in-toto+json
