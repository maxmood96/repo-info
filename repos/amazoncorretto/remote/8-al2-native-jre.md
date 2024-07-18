## `amazoncorretto:8-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:51e574b3c34619e5fa1aa5f956f5868725ea24ebf7c69c4a3e29b13c31f431f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f582ec5751671ab1a46ee58495579eff22605fb49b2e689add2413719d044115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.8 MB (171776119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c0472e48654139eda7eec73e966eb33dcef175f7b0bc3e6cd6ba82c68a4dbf7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Jun 2024 00:19:55 GMT
COPY dir:db8dc48874881c2542c8e2120173f53413158e7da7526edf07aa742f426b8c16 in / 
# Fri, 28 Jun 2024 00:19:56 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=1.8.0_422.b05-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=1.8.0_422.b05-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:2a5dc0ac7266321476902a4277a4723285b608c065fcb80cacdb3ed43a7c29fe`  
		Last Modified: Fri, 28 Jun 2024 00:20:37 GMT  
		Size: 62.6 MB (62646638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ee6c79a702766f595abc91d10272454891bf0f6fbf61bcef3eebebed08bfd36`  
		Last Modified: Thu, 18 Jul 2024 00:56:02 GMT  
		Size: 109.1 MB (109129481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9bbd5920db7f08cba0316889f13adb68119c838f0d66e105541998cf693bc0c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7506980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e512799eaa58c725dc1cfc455143574d7b60e65c51872ea193eab008e37bd11b`

```dockerfile
```

-	Layers:
	-	`sha256:97832d91c2e7cef877042f4526608b6d2c9678d094030aa83e659395a1c9c840`  
		Last Modified: Thu, 18 Jul 2024 00:56:01 GMT  
		Size: 7.5 MB (7497672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6a5819c22f88cdcfc56981f17827a4cf41146846a42e3be1c1cd3d9b7fc9a80`  
		Last Modified: Thu, 18 Jul 2024 00:56:01 GMT  
		Size: 9.3 KB (9308 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b9eb3fdddadb0b0b42742e05668e1c2448b07d238aef0d505cd2c1149ac648d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117508616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d97a99b99b66a97a3f633eabcd00b446bcba2afd4ceab03d3e6ab90070836da`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 28 Jun 2024 00:40:02 GMT
COPY dir:36542351efcfebe46f7ccbf0def8f62c4d1fc618b41a02b6d9df97e06c5cf74a in / 
# Fri, 28 Jun 2024 00:40:03 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=1.8.0_422.b05-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=1.8.0_422.b05-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:2936210a619ec662b53521cc3dd41798a491971a48e14f14ebb594e81dc798b0`  
		Last Modified: Fri, 28 Jun 2024 00:40:34 GMT  
		Size: 64.6 MB (64568765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5345fb81fd035b1068901f84de231adebca9dc6e29f8aaddb2fb47261a802bb`  
		Last Modified: Thu, 18 Jul 2024 00:57:16 GMT  
		Size: 52.9 MB (52939851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:202333487182ee8ecc990b160861faac44a816d3a6c1e43be2b14f3f2f943595
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5623002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a30a6bf05c4c8c1523094760f15ee24013bd7a43868d49a57d39124f490ce8a`

```dockerfile
```

-	Layers:
	-	`sha256:de83143de4c7829786c385f8d74dd26f99b14a8b5eab633e385fdc0f6fca7f7c`  
		Last Modified: Thu, 18 Jul 2024 00:57:15 GMT  
		Size: 5.6 MB (5613416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96012ff228bae99116b86ed8394f8de4d41cdc3a6672c9a1f418db54f4b308b8`  
		Last Modified: Thu, 18 Jul 2024 00:57:14 GMT  
		Size: 9.6 KB (9586 bytes)  
		MIME: application/vnd.in-toto+json
