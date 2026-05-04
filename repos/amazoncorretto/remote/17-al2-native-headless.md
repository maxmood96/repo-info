## `amazoncorretto:17-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:8f689b00acd5db1f3aa71af9daa69311c0840fdbed8fbd9657586c61fc942df5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:410f305d8dfc1a525a9d52d24b6ae17f0744b43fdf5c9326d7c471f85d79eaf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.5 MB (150510933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80edb2a38f70dcc76ac47b067248b3e8e009d752fe2aa42580e076d408765ce2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 04 May 2026 19:39:12 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:39:12 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:12:35 GMT
ARG version=17.0.19.10-1
# Mon, 04 May 2026 20:12:35 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Mon, 04 May 2026 20:12:35 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:12:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:1deb63baef8049d37b87192670264bba74a0207718cc43a1c66077f5bf81a3c8`  
		Last Modified: Sat, 02 May 2026 04:14:38 GMT  
		Size: 62.9 MB (62860009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ceeb6a28cfb0c8baa2f6b1c323584157bfea5e93e4f4b35e43e13415ad483d`  
		Last Modified: Mon, 04 May 2026 20:12:52 GMT  
		Size: 87.7 MB (87650924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:913455e5fa1815274353004eac7133c1cc77811fc7da36ec0abaf20561afa22f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5642142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048b3eff6ec79cfd174bfeb344a46260d5182ed913b128511d819f775009796b`

```dockerfile
```

-	Layers:
	-	`sha256:889ae5d291846f1d21f7f13193d4259de5be3aa9f573b570015199b69fb5aa58`  
		Last Modified: Mon, 04 May 2026 20:12:50 GMT  
		Size: 5.6 MB (5632679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:947a95362cdb837bc92ebf791173fbad38a9c81f3af6cc098655f9c86ba8e10b`  
		Last Modified: Mon, 04 May 2026 20:12:50 GMT  
		Size: 9.5 KB (9463 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:4c7d1a174c1bfaf57da5fe79aeef8d3987668325164fd5d368fa4aaacbf6999c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144737261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aa98d7ed4e675929933be1576d122fbc62dc88dfc022395ce4f868916a723c8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 04 May 2026 19:40:38 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:40:38 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:12:21 GMT
ARG version=17.0.19.10-1
# Mon, 04 May 2026 20:12:21 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Mon, 04 May 2026 20:12:21 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:12:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:d78bec86efed585192790ef27ca98e5305604b02ec838239205e149e3aff726c`  
		Last Modified: Mon, 04 May 2026 10:12:23 GMT  
		Size: 64.8 MB (64795531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78f6115700b73a6eddb86e1b5cd1668ad0643941e480896befbfda52a50014c`  
		Last Modified: Mon, 04 May 2026 20:12:38 GMT  
		Size: 79.9 MB (79941730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6ff7c55223b2efbe3568b525dd01be3ec1eb161306f7f0a94e7ab360b0388e2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5458499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd2aeb995e2bbd167b64478c0f123db9189ba20c2afe23e889203a8c496f1b99`

```dockerfile
```

-	Layers:
	-	`sha256:6b1a3fc6681c25de0eb08eaa022a9ee22adb06d0d9e8b65d649203768b963518`  
		Last Modified: Mon, 04 May 2026 20:12:36 GMT  
		Size: 5.4 MB (5448956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:748c536a815902dc44bbba52a1979deae05ac29df5633156e8ed4693d4d96d04`  
		Last Modified: Mon, 04 May 2026 20:12:36 GMT  
		Size: 9.5 KB (9543 bytes)  
		MIME: application/vnd.in-toto+json
