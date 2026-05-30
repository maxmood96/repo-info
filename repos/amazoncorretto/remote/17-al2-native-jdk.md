## `amazoncorretto:17-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:5b12583e7c6ff79d0c36593930dcffcec0629e8304087d9e776b91ce72f6960d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3fe64689656e7218aae2393a22a8a01d9b49f59bdb014284543ffce180768d5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228914738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48de97874b60bbbddc7d3c20587f63cb8806b18a5b288c7419e6f80b0949c1a2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 30 May 2026 00:27:01 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:27:01 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:12:27 GMT
ARG version=17.0.19.10-1
# Sat, 30 May 2026 01:12:27 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2.1.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Sat, 30 May 2026 01:12:27 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:12:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:1b617831d6b1041202bed08e227be201a09f5bbe282304143d3ba1e6b9b6cd1e`  
		Last Modified: Wed, 27 May 2026 11:49:15 GMT  
		Size: 62.9 MB (62941950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b61850d1d60f0b8c0bfebdca7e0d1cdba1027fda61009645f21695bc2bbd7fb8`  
		Last Modified: Sat, 30 May 2026 01:12:49 GMT  
		Size: 166.0 MB (165972788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5afec9c10a81b6b9cb3621f467e62bac06a2a1bd405823969ba3b45068350bdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5982800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c4c844880ab1ced4c2677e1128af3883e659b248cf966ec4085e9a2e2d20e9b`

```dockerfile
```

-	Layers:
	-	`sha256:acf32367aecd6e2c19973beeb03c3175254a488b4e91e53b3ad0d1c01f86d802`  
		Last Modified: Sat, 30 May 2026 01:12:45 GMT  
		Size: 6.0 MB (5972740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f1b6983f793e5b4026577bef5996b7b9a63e5cb4496b4bef29ec5b20c258fca`  
		Last Modified: Sat, 30 May 2026 01:12:45 GMT  
		Size: 10.1 KB (10060 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e969e9dd92685923e051e145f8cee8b3d8748505ea1bf1e09f017d4956700a2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.3 MB (221263832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83185801a258140c32dc76796c9f7632f7e76cc4f67ea2d2d64848a884145577`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 30 May 2026 00:29:01 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:29:01 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:12:18 GMT
ARG version=17.0.19.10-1
# Sat, 30 May 2026 01:12:18 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2.1.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Sat, 30 May 2026 01:12:18 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:12:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:592be6a6d0447cc7e4d0cd5d164508693821dd45a5dbe90f47689441f936d50c`  
		Last Modified: Thu, 28 May 2026 09:28:16 GMT  
		Size: 64.8 MB (64790709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81f08c736705dca09348de77d86dd0fa14c42fb0d04ac6df328b02872c82b0d`  
		Last Modified: Sat, 30 May 2026 01:12:41 GMT  
		Size: 156.5 MB (156473123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:107fb82e8407cde0f4b77ebea9e6acbf4643d02285da3883dffa54dfd440a5dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5774750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ef3784ec298af35f55af1c7ef0ad09a8149dd56570f6a48830457eb4cde1a47`

```dockerfile
```

-	Layers:
	-	`sha256:ba5579871f1eeeaa9e5e81b6255fa6e8142fbc462c1e5799b06d523823b57dce`  
		Last Modified: Sat, 30 May 2026 01:12:37 GMT  
		Size: 5.8 MB (5764611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef15586ca5f91f2252682595c717c0b4ef37730b80e36db5b9b8c5f1447dbe5b`  
		Last Modified: Sat, 30 May 2026 01:12:37 GMT  
		Size: 10.1 KB (10139 bytes)  
		MIME: application/vnd.in-toto+json
