## `amazoncorretto:17-al2-native-headful`

```console
$ docker pull amazoncorretto@sha256:0dbbd75541bba5218267bb85c874ab5f2117c4514ff7b8d4048157e279b47952
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9c207e257467a40f8f8aefba94de842f3b2592de7202e3f32ed76613d00e833b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.1 MB (154118791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:657bca29e3c607840a6dd1badf1fafe8038ae5512ea02edf604e864ccf5591c0`
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
	-	`sha256:78d6b943ec35657899afc44f3f9b766ee923d9028028da721b7d4e7bc35e184f`  
		Last Modified: Tue, 23 Jul 2024 13:50:25 GMT  
		Size: 62.7 MB (62679166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03cd488f713d00b80c64ac421e0bf29df7ec8d415e47f82ff3cb20f43762511f`  
		Last Modified: Thu, 25 Jul 2024 21:02:35 GMT  
		Size: 91.4 MB (91439625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9a601f5b200f48f94582d8b9467fcb596b6ae87f5f98aad80a33064a1253e01c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5869496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2773746722e9e0748a68e16178acd653761dc7bf8d6dfb7a8d282029375b7ce1`

```dockerfile
```

-	Layers:
	-	`sha256:3d17ed04194776b4e7cc4672405b45a9cce7e7338e85a72eb14335ad2ca53536`  
		Last Modified: Thu, 25 Jul 2024 21:02:32 GMT  
		Size: 5.9 MB (5860059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfeef79bf15fcb22ddce5e56551e6d96a8c8b4a3d0ac231e95a26d335912acd0`  
		Last Modified: Thu, 25 Jul 2024 21:02:32 GMT  
		Size: 9.4 KB (9437 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:70e8f9c145bafdc5731ecab9a513e57c5e0430e984199b30a10c9eecdb1e9695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.8 MB (146779494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1924fb5ee05fc721f114308f43c976de4511ffc2fd63575a22800b55cbdad26`
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
	-	`sha256:90f49a0942af5d23537faf4773696e5a1ede92273c5b8379a6acc52111436bb8`  
		Last Modified: Tue, 20 Aug 2024 21:34:48 GMT  
		Size: 64.6 MB (64587135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45dbf40b5bfd2a2f1d5e5e2b4d5c32cc4583fd105626ae67b5822f4eb15b020`  
		Last Modified: Fri, 23 Aug 2024 02:30:51 GMT  
		Size: 82.2 MB (82192359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4e16a7bdea7c319796b413e4300eaf9058cb4c7ec2b278978404b49b3dcab3a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5661275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:773b7f61f99597b8e31825f785cd18208ca2c3c8bec6d22ce4871a9447310644`

```dockerfile
```

-	Layers:
	-	`sha256:f3c74c8643b7620c51d6bf1168cb32553e5ff82b588b98a8d398b82b403ebbf6`  
		Last Modified: Fri, 23 Aug 2024 02:30:48 GMT  
		Size: 5.7 MB (5651477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:231047d352147fd22a6de1c094d19872ac7e202cd1c37068a35d015f20b03eca`  
		Last Modified: Fri, 23 Aug 2024 02:30:48 GMT  
		Size: 9.8 KB (9798 bytes)  
		MIME: application/vnd.in-toto+json
