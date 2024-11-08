## `amazoncorretto:8-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:be56f7cb854a1a0895cc3d096b28b16d930436d5ec089817f6d13a7760e4e5ea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6dafe152c5245d7bac763dcc3ecd45bcdc196bbb3bb6f7ec387e800b31d60b4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.9 MB (187921306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24f9a3a45d5da9868e220410bf88777246e218a920d1f361ce74b9d5ca4227fb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=1.8.0_432.b06-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=1.8.0_432.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:8430d4c5a00587f0a8dc4c62f82455c123b54b9016d43897ee77c496c018a8bd`  
		Last Modified: Wed, 06 Nov 2024 20:48:04 GMT  
		Size: 62.7 MB (62681042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0bb3e99053e5410f1344fd4abf629dff81bd1b7df07ad4f7dd950a4fa38e9a`  
		Last Modified: Thu, 07 Nov 2024 21:48:13 GMT  
		Size: 125.2 MB (125240264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:eb16c718244fb220ae833bb5142302b67167c5d7ada0663fdde3e288158af9a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7980844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d20fd88008813e4f676fdffd2114b8901e8ef0015957e551b40816dbcc5d84e`

```dockerfile
```

-	Layers:
	-	`sha256:b90ccb7563a2f856c72d9df2e131114e6b09b310afe6eacb3ee1bf98d45f43c8`  
		Last Modified: Thu, 07 Nov 2024 21:48:11 GMT  
		Size: 8.0 MB (7971252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e18debddc7fbd13d0368f0cb9770cf3b6da309a302d158c9e9e08c47afc11bf7`  
		Last Modified: Thu, 07 Nov 2024 21:48:11 GMT  
		Size: 9.6 KB (9592 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d9dfa884dbfe3aa04111458827465fc68ddbae32eee573c68b5059c73a4ddc87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.1 MB (132143099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e60dc0b14b305f844651a189f35e6a9d3f584064678742c780b3ccb35a26989`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=1.8.0_432.b06-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=1.8.0_432.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:0a62aca1c7d7ec3e0e098bf23685d8f0fcd19e33577a91dafc6dd30bef06deca`  
		Last Modified: Wed, 06 Nov 2024 20:48:17 GMT  
		Size: 64.6 MB (64588571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff0c4981fa23ebb568fbe509145be8d8108fa0321aa23b7fdcc173d63ab9ba3`  
		Last Modified: Thu, 07 Nov 2024 21:50:02 GMT  
		Size: 67.6 MB (67554528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:081587e98d35ea16db316a1863e365d5eda80005401783dfada934e5f3ca6b58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6087428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96a089cc93209d61559bc8ccfd0e4ee0537ac75974c1156cc375f01dc2941142`

```dockerfile
```

-	Layers:
	-	`sha256:59e93e33a4be85f15b593dbd3929ad33b2e372436ed7bea6199b8b2efa5ce720`  
		Last Modified: Thu, 07 Nov 2024 21:50:00 GMT  
		Size: 6.1 MB (6077757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd97e55071a17b67369da569c9333b3a84efd23e48b9a2636bb2c6e25cf5c799`  
		Last Modified: Thu, 07 Nov 2024 21:49:59 GMT  
		Size: 9.7 KB (9671 bytes)  
		MIME: application/vnd.in-toto+json
