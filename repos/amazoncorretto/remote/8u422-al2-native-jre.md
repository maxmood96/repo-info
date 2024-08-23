## `amazoncorretto:8u422-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:9a4273c1d6a9e9ca5fff3fcda9e18ac94861b71c319f883b4a1795c531d3cf16
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u422-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:bfd02641fbefccfacd66f3dcb4c01b9b764ae611aba5409f0546763155a47916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171850785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d82a0ad5c65b1f51f5eb38baa2b721fc61efaf227da4398b984d77439a6fe62a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
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
	-	`sha256:78d6b943ec35657899afc44f3f9b766ee923d9028028da721b7d4e7bc35e184f`  
		Last Modified: Tue, 23 Jul 2024 13:50:25 GMT  
		Size: 62.7 MB (62679166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c91bf364720aa675eb26c6599e062fca09cf8bafb6d8f079db9292d77dc7361`  
		Last Modified: Thu, 25 Jul 2024 21:01:35 GMT  
		Size: 109.2 MB (109171619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u422-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e55d46d95639a93fb1c7e884fccdeda166179a57cdff60fbb73d11c851aba699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7507186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2111bb055b25ee9e08641e4b56ace41d9deb68a59b132ec9f334b21c5685878a`

```dockerfile
```

-	Layers:
	-	`sha256:8aca6ac1371243592f0d921249bc2128da07bb296308a20923f482c3919b104a`  
		Last Modified: Thu, 25 Jul 2024 21:01:32 GMT  
		Size: 7.5 MB (7497672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc4688f60d140fb4fc9941581a65bb29faf589aa5d4e02bb872c83530763de72`  
		Last Modified: Thu, 25 Jul 2024 21:01:31 GMT  
		Size: 9.5 KB (9514 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u422-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0f1c288f45e6e1c73469c789564789cb6346a6ba0a0b6576b076ae3e698f38c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117523252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eb5ab7db205182174b0806f20933bee32948092019d9cbe8ee5afc79e4f39be`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
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
	-	`sha256:90f49a0942af5d23537faf4773696e5a1ede92273c5b8379a6acc52111436bb8`  
		Last Modified: Tue, 20 Aug 2024 21:34:48 GMT  
		Size: 64.6 MB (64587135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073a76f5c44506982b7eb54b2f9622707d5bf9bf66d769b1f089a41e685b27d2`  
		Last Modified: Fri, 23 Aug 2024 02:17:51 GMT  
		Size: 52.9 MB (52936117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u422-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:53e9dfaa7513cd48a46e461f15a0106cbcb1a5025bfebd7c3cdd30b249891f59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5623306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d74d1f6775571932830d97b4ef32b85b106f679808ac7b70da2cfdb1b54b0db`

```dockerfile
```

-	Layers:
	-	`sha256:38997ee312f54e8c3bedf1a7d33e29d31112a7a9b15b21d9a22064402a530278`  
		Last Modified: Fri, 23 Aug 2024 02:17:49 GMT  
		Size: 5.6 MB (5613432 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bc80b6e0bef6cb99cbc515c871fc5c4ee6070e4acc10f4305fa7ecf9fa627bc`  
		Last Modified: Fri, 23 Aug 2024 02:17:49 GMT  
		Size: 9.9 KB (9874 bytes)  
		MIME: application/vnd.in-toto+json
