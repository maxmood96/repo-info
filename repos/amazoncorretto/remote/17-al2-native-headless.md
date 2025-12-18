## `amazoncorretto:17-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:ab0eaa6a676037e23101868123f2b402b8771764e4497af704a4fbdbce63f8eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9b052bddf494fb074900b0a4552f8bb472d34a0cfde6c4de797ec90787fa7b5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.5 MB (150543514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a8c6c823a0842309975d9d61b0b0762036456986756a5e701f43702826d30e5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:55 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:55 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 01:18:29 GMT
ARG version=17.0.17.10-1
# Thu, 18 Dec 2025 01:18:29 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 18 Dec 2025 01:18:29 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:18:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:364e8e668f0e62a54627e7d364c5d2a3a16f70f1c962628fd84b9ef8fb667d21`  
		Last Modified: Thu, 11 Dec 2025 05:04:46 GMT  
		Size: 62.9 MB (62940975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51cbea01ca9e8cffca09341d1a2a8aceb8fe348871173f1e01f668e763fb2128`  
		Last Modified: Thu, 18 Dec 2025 01:19:02 GMT  
		Size: 87.6 MB (87602539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:63ac29b89f955141af087b8f558c8cf570ced7a9285dbddd47f3ab97d25e7bc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5641057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f3a16721bbe737d16af6d9f17a0495008efc157f4324d4e8035fde60a6c3a3d`

```dockerfile
```

-	Layers:
	-	`sha256:73c201e60f0bcfa8e8f814bc67aff628156483afd39170b72b7e90f3f475f833`  
		Last Modified: Thu, 18 Dec 2025 04:48:53 GMT  
		Size: 5.6 MB (5631763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5d752db3cad5b21750190d9d759773e2fea9ba8361225a29546d9d33f7b398b`  
		Last Modified: Thu, 18 Dec 2025 04:48:54 GMT  
		Size: 9.3 KB (9294 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:3c52b92019a2c5c4fae806976aaff4b37b76c933a90f8c17e3ef6f54aed82400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144623617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfaf4cc4e53af35a90684b695cf063c9fd937287e31028527df2fffff59f1768`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:41 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:41 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 01:26:29 GMT
ARG version=17.0.17.10-1
# Thu, 18 Dec 2025 01:26:29 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 18 Dec 2025 01:26:29 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:26:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:535c61639a173696e963cd2ada71746467bbf8ddd232fde633f87067e08137f5`  
		Last Modified: Thu, 11 Dec 2025 21:46:54 GMT  
		Size: 64.8 MB (64795755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3945fbc38b4a45020af107741c2cba5edc4a3353553107799ae03a5fb26136`  
		Last Modified: Thu, 18 Dec 2025 01:26:56 GMT  
		Size: 79.8 MB (79827862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5cfe55a3e04845458be1632b1967a7c941fce2229fd92d6e9ae1d11f8d3f966f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5457413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06469dce5ddaf6e8ac7c52a90499c7bc55b511e170c7f7e2a4075a57d2626245`

```dockerfile
```

-	Layers:
	-	`sha256:cfad60ad94481bf7062cd3b1d4c8b55abdb10a1f14a91d1d1b2b506dda58ccb8`  
		Last Modified: Thu, 18 Dec 2025 04:48:59 GMT  
		Size: 5.4 MB (5448039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd7fde5ce2160879000fc49da1d90f105aac1e5a2d35af4a0f21d66a8c2bc015`  
		Last Modified: Thu, 18 Dec 2025 04:49:00 GMT  
		Size: 9.4 KB (9374 bytes)  
		MIME: application/vnd.in-toto+json
