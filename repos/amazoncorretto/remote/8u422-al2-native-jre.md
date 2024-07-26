## `amazoncorretto:8u422-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:9ef186dde150f7bd65ca0761103bcc96d2ee90cab88cdb994a6e9f24ffa08c30
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
$ docker pull amazoncorretto@sha256:7713f0547f4a8a3277af98554418e83c08e888aa543c14599475d1c93e80c9e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117512667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c4d91c5b956fb0a7f52093e24529d4996ece9ddd45fae2fb28d747e82a808c4`
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
	-	`sha256:7ae84cee97a8a17573116f568e78a8d7c8415a733e0ccb92185dd2e22634f9c6`  
		Last Modified: Tue, 23 Jul 2024 13:50:38 GMT  
		Size: 64.6 MB (64572700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d287f461f0339cadd02c16d6ecd618e1887074766fff3590ac9dea0a96e016df`  
		Last Modified: Fri, 26 Jul 2024 01:47:47 GMT  
		Size: 52.9 MB (52939967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u422-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0745124f775bf631d956d57a6c94243947577def4e9a2c4df5e20a0fb8bfa056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5623290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa2d6e5fa5edac43926c48d1ac8ba2535fdb8d6e5446189946d981f6faaf19c`

```dockerfile
```

-	Layers:
	-	`sha256:b82be83e9d9320265890211c11306f7c9681df97f99aed3d62bf4d3ee30ec866`  
		Last Modified: Fri, 26 Jul 2024 01:47:45 GMT  
		Size: 5.6 MB (5613416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b4edb68d7f8623d20536f3115a12bdca0431d95d5fe55700332f12fd8abacdb`  
		Last Modified: Fri, 26 Jul 2024 01:47:45 GMT  
		Size: 9.9 KB (9874 bytes)  
		MIME: application/vnd.in-toto+json
