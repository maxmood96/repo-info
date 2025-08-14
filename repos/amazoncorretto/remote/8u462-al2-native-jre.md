## `amazoncorretto:8u462-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:5ffcb5aa42dfc9ede7f8159d985e6259b004d593e333e34185c7d328c73e00d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u462-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:43eb0e90909310943d7b272dd8d3a4be7ee7cd7c9e3a5be597c6ce2a45249b5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.1 MB (172109568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d6dc1c14643602ee2cb8cdce91ee1a817e089b78bf3a17dc61c49ad11bf3d6f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=1.8.0_462.b08-1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=1.8.0_462.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:dcefe03e9009da4739e237894f3fe49af6782d53d9e2202e46127bd568617855`  
		Last Modified: Sat, 09 Aug 2025 04:15:21 GMT  
		Size: 63.0 MB (62959372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa78f2e02cfb448cfe9ad9c9fa7239f83f9738a5028427cce45c1bdb818cc21d`  
		Last Modified: Thu, 14 Aug 2025 10:37:51 GMT  
		Size: 109.2 MB (109150196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u462-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5affc78079d81eb47d9bd7d0ef40941ddf333b063c1b22ee74e89da76741a1a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7513668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:616489f6733bf5276885033238afdba08e25ed2ac443b0b467964fa4b3a34da9`

```dockerfile
```

-	Layers:
	-	`sha256:c67295865bcbc389f40fbd5ca6e5056031695b910e20c4cf37c36dbf31e1fb2c`  
		Last Modified: Thu, 14 Aug 2025 00:50:08 GMT  
		Size: 7.5 MB (7504120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f755254f49587cbac714a0497ed0ff747ca3f896526cd715e78de7aa54ee876`  
		Last Modified: Thu, 14 Aug 2025 00:50:09 GMT  
		Size: 9.5 KB (9548 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u462-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:19d5a9d7ea68f519c408c99fbc358f8646283eb84cab15bff3ea62d96015980d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.7 MB (117729002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38cee29d3afc7cdc8345082df46e6d39f138d0fbc36db9c0cec140f4c1e59c7e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=1.8.0_462.b08-1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=1.8.0_462.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:2c5df7aef58ef9598380ed47447cb5a8a274be6648b1015fa328f378b9e2da76`  
		Last Modified: Wed, 13 Aug 2025 22:57:44 GMT  
		Size: 64.8 MB (64794364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14735472dfe7e8cf1e1ab59ea8a64198e740ce33a3be8e61fef5afc74552d5ce`  
		Last Modified: Thu, 14 Aug 2025 08:50:24 GMT  
		Size: 52.9 MB (52934638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u462-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:016dc5042e925f575b102072a44416b9aae58dba73cdfd33925fb4a89d2d938c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5628514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:391cf4b60dc3bb16632052b89cad1b8c1b0c3dfd79e0d8710ee3eed79774537e`

```dockerfile
```

-	Layers:
	-	`sha256:218358102bf27da68a2d838ede6a58998a72802e495b0bf94f3450b859f64555`  
		Last Modified: Thu, 14 Aug 2025 09:49:53 GMT  
		Size: 5.6 MB (5618887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b61dc418bf9dc7f12dbe116b2f53b2fb3d7022c1b5f989644472051e7aa8b247`  
		Last Modified: Thu, 14 Aug 2025 09:49:54 GMT  
		Size: 9.6 KB (9627 bytes)  
		MIME: application/vnd.in-toto+json
