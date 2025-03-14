## `amazoncorretto:8-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:09f0a33834c3c30c5722d1c69521220e72bc1e0a4f5d744935e148a205acbfb7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:932648ce6f91e7198cc5437bbc011ea8da772b485bd747178e370ed9b60ee3b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.0 MB (188030230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdc0f01470b2fcfd6a9ab264153f1a880e18516368ba366666b1181872f86780`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=1.8.0_442.b06-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=1.8.0_442.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:f3dc83dc2e4e000fd189efee126db80e38a079b47b8e5229a794a0a6148bfec6`  
		Last Modified: Sat, 08 Mar 2025 04:13:59 GMT  
		Size: 62.8 MB (62772838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfeda5cb5c246f1c7d89475945ca8cf02cd1f9b22d025e77b8d153fe32a96f6c`  
		Last Modified: Thu, 13 Mar 2025 22:53:28 GMT  
		Size: 125.3 MB (125257392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:978574d4724d76d9d034f22323f2e1476bef4f8b30bb3ec1ccf23cec88e72417
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7966109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b6fab5f9c2471835abff03513506900d178c2a964e22092104f1679b290473`

```dockerfile
```

-	Layers:
	-	`sha256:e3e875f4a1f7c1cef81c5cff58c3de7ddf2d5dc84dd454ba4fc57e4a567274fb`  
		Last Modified: Thu, 13 Mar 2025 22:53:25 GMT  
		Size: 8.0 MB (7956516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:498ae4d35a5e380222644559f2f0f4a8affcbc4c4b214ed0464790a3e1b12450`  
		Last Modified: Thu, 13 Mar 2025 22:53:24 GMT  
		Size: 9.6 KB (9593 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:71cf947198b6642ca40c2b4cff5fb9b22046f0b35c8a41ac77c9584f1a591681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.0 MB (132032741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65cff4a753d7f9cdb31242f73e6cf9ae57eefe8afb3bb8e5c88b95a39f0c2ffc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=1.8.0_442.b06-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=1.8.0_442.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:5270c35d4d9446d8a0ab2f41ab0020c11889bd8617236093cc9c87563d120b9e`  
		Last Modified: Wed, 26 Feb 2025 15:57:39 GMT  
		Size: 64.5 MB (64521208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba06997272c028070299f4f943d38670106fcbce0671df21d308211e437160f`  
		Last Modified: Thu, 27 Feb 2025 21:10:04 GMT  
		Size: 67.5 MB (67511533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9df36d57611f0ce04f8ec87646b8c7ad8a5bfb5cd7bf6b2347e237c541aa2d5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6076351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6131989cd281527a48c416c029fdbf5f59105bff0d79eabd589663bdf7b95335`

```dockerfile
```

-	Layers:
	-	`sha256:e5b83d49732fa7e1818f111418ce38e725534a6257eafe9cfee4b7724d7a50e4`  
		Last Modified: Thu, 27 Feb 2025 21:10:01 GMT  
		Size: 6.1 MB (6066679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba81f62715622967981b28a09469734b45c5ab469f7194af5215752248868caa`  
		Last Modified: Thu, 27 Feb 2025 21:10:01 GMT  
		Size: 9.7 KB (9672 bytes)  
		MIME: application/vnd.in-toto+json
