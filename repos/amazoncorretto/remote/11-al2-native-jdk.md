## `amazoncorretto:11-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:0bb980c17aa7861e13348a386c48b30106a99808d0d7b3c0d2f8b23e411d073a
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
$ docker pull amazoncorretto@sha256:1027b48f52bf2436d4510cb8e416319f19f9fdd31ad9bc7925726ac6ffdb732a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.9 MB (216870013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6203aa06e8e8d4f7cc421b48634a0fa3f96e2e1846e063f4fcbcad10d7a34a0f`
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
	-	`sha256:90f49a0942af5d23537faf4773696e5a1ede92273c5b8379a6acc52111436bb8`  
		Last Modified: Tue, 20 Aug 2024 21:34:48 GMT  
		Size: 64.6 MB (64587135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3866c6db913d2a3c4b00b80e7cf5572d3f8fff5e96c04c546ea7b0c5e38f84`  
		Last Modified: Fri, 23 Aug 2024 02:24:28 GMT  
		Size: 152.3 MB (152282878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a383275785c4266869e4f71182761f70bfbd36383b7b00a24045381c60349916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5792467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ea82dfdbd99fda2ce7f842d10a954b59682614af62fcc1c907d67753b5bd95`

```dockerfile
```

-	Layers:
	-	`sha256:3eb3362e4dde92b2aa33091438fcb17f71dc5d522d883c62a2af2684dd2d02e2`  
		Last Modified: Fri, 23 Aug 2024 02:24:24 GMT  
		Size: 5.8 MB (5782700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0080264c6d1b49212677be879459f761f5a837ffcd56c8b83ccf7913c79b5314`  
		Last Modified: Fri, 23 Aug 2024 02:24:23 GMT  
		Size: 9.8 KB (9767 bytes)  
		MIME: application/vnd.in-toto+json
