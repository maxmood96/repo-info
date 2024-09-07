## `amazoncorretto:11-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:272a550fb1fbfe96585257e89039141a2c0096dea9fe31194379665d788fc587
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4089a888fe4996f261ba6e4309417110cd5dcbf2a9e8ab9b4e3ef4adaad13a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.8 MB (224842762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:824981e03d47160e470ae1000cf7bfb74185e6409925c7205edecf9a7f8bdbd0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=11.0.24.8-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:7f8efc14a219454ff8f309d236d31a55327a6ff05dda42df51689619d9a34fdc`  
		Last Modified: Fri, 06 Sep 2024 18:59:36 GMT  
		Size: 62.7 MB (62695547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a793c7cf183121e5e3322d9ee6b70cc020345eec4042f1abf14cb9c47bd3efc9`  
		Last Modified: Sat, 07 Sep 2024 01:06:06 GMT  
		Size: 162.1 MB (162147215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0f2bad4e6614ad413a291be474cc6f62a1704c3dab98de722796def4ce621f66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5999731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:171f2feba665712d88a65ea49e17c84de3ad3c8e884f9d6d7fb0df0efb914fd8`

```dockerfile
```

-	Layers:
	-	`sha256:ad1eb22d4a8004b1136620f8526f62700323b366a81bb7ad45194cdc3cecc406`  
		Last Modified: Sat, 07 Sep 2024 01:06:04 GMT  
		Size: 6.0 MB (5990325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2621b742ebd1975b6a881aec0cc9d5a1a24c9c0c07b179ffe0457fd342d1b923`  
		Last Modified: Sat, 07 Sep 2024 01:06:04 GMT  
		Size: 9.4 KB (9406 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ab2e4f2a40d589bb45b5ae240865335964f06a12fdef166955f7dde7366599c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.9 MB (216869096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b93be673e202320d4d376bf5862f1dc16e5d4fddcbbf7bf845a79ee7ffc0e85a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=11.0.24.8-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:0f0968c920788bb8a898446e0bbe8ea6b11fcbf7f55810ef51044775a045d6c9`  
		Last Modified: Fri, 06 Sep 2024 18:59:50 GMT  
		Size: 64.6 MB (64586343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904d79e1e67f962211cdb9add50fb089ffff8cc4dc766c05d38d86d3be2dbb10`  
		Last Modified: Sat, 07 Sep 2024 13:17:11 GMT  
		Size: 152.3 MB (152282753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:97b3f17d51624bf479f4a6909d1371e16018bb41163f97d5a1043a37b75da44d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5792467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a910d8611edee2992c446ae162d3209da2fd50e0a6ab698eb6d30c1a49532b2`

```dockerfile
```

-	Layers:
	-	`sha256:fb8f35c052ac238d688aea38851748a14b4c908024444da8ffc61af25d40d98f`  
		Last Modified: Sat, 07 Sep 2024 13:17:08 GMT  
		Size: 5.8 MB (5782700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94df46d8aa59a79e422ef607160ebf908eaf9f52fa8e5fb41ebf682023cfb6ef`  
		Last Modified: Sat, 07 Sep 2024 13:17:08 GMT  
		Size: 9.8 KB (9767 bytes)  
		MIME: application/vnd.in-toto+json
