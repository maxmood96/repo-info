## `amazoncorretto:11-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:eaaabdc5e1810a2bf4a94cc39b9cee7feef4699b9c18b68f6cf5b23f649faa69
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4c731588ff29cd987959f336ec6e4d7f12aa58bb81c4d9723dacb330e9512edd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.9 MB (217939234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd353dc4ac19763659c758b9288332ba33b07dac9f6822d1451b1bf44e41a7e5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=11.0.27.6-1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=11.0.27.6-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:59c3b062666ba29c100bd47e4ef63a7010fdd4d56e4483d5f68f9ba709e6f55c`  
		Last Modified: Wed, 25 Jun 2025 09:50:04 GMT  
		Size: 63.0 MB (62962854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2795b6c6f999ca4dea8b11ac600037a3ceae0823e99bf3f7e28bdd64bf78c33`  
		Last Modified: Fri, 04 Jul 2025 03:21:48 GMT  
		Size: 155.0 MB (154976380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ac6640d0b75b5da218bcc771204395cb00b2695105c7ac69b07f809f446d91fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5692632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db622efddaf10dd8368b73f9c57f34c01d483df15e36bda28d8c8a9f72b38236`

```dockerfile
```

-	Layers:
	-	`sha256:d337d45785a676f945f7c6a22c3a465054c137c5e94b220a41836dcfffa673f0`  
		Last Modified: Fri, 04 Jul 2025 00:47:26 GMT  
		Size: 5.7 MB (5683301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da34dec43e7197133b154643123b3c5605cb7ae90e5fe9429cec3f83013c7a02`  
		Last Modified: Fri, 04 Jul 2025 00:47:27 GMT  
		Size: 9.3 KB (9331 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e1c2c7fd277d922ef9851c8cdb0ab4b5c968acc737d539f1ad9e2dba9301eb3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.1 MB (212084745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a58b622cc5614f260a3a5e6fa9fe2c483bce1166d1fb911676ea2424e3737aa`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=11.0.27.6-1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=11.0.27.6-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:409bf1beed8b3d18aa6739b3b654d78ea6e9842b177c58b3fde860845eae1b51`  
		Last Modified: Wed, 25 Jun 2025 19:30:21 GMT  
		Size: 64.8 MB (64794781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e9a2bef807792b3d2841491b803c4d43d585975d6c56d407202040f65eb7e4`  
		Last Modified: Fri, 04 Jul 2025 14:23:13 GMT  
		Size: 147.3 MB (147289964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:339e4e7f3c277e789596924f361e9e2bdb0c4578dca8db5a1d2ae97d9bd7f0bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5511179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d9976caf57b7b66d2458079ff227a5affd9625225301e67a9b932c17ce8a8b8`

```dockerfile
```

-	Layers:
	-	`sha256:80c1c0bfa474bebd9677c76dd3e186a9a6ff046d276b2707cb0553ca803a7912`  
		Last Modified: Fri, 04 Jul 2025 03:47:28 GMT  
		Size: 5.5 MB (5501769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f39ef0c45bdfd4947b49b67ae4608b4e1d4741ba1faa37b025b611a81746cdc`  
		Last Modified: Fri, 04 Jul 2025 03:47:28 GMT  
		Size: 9.4 KB (9410 bytes)  
		MIME: application/vnd.in-toto+json
