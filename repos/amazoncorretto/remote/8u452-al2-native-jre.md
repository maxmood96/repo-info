## `amazoncorretto:8u452-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:51b4a4f1099810e7cd6d3535add6ac821bb190674024e4a3908cd34ee2dc266d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u452-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f75b74b8d376732f159f2f56f2480a79c6868462d0d0432c0fc7a76329eb4bb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.8 MB (171844595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d0673be025414a667805dab48615ce7796fd9e2aa440680ea570d62f8087b47`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Mar 2025 17:58:37 GMT
COPY /rootfs/ / # buildkit
# Thu, 27 Mar 2025 17:58:37 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=1.8.0_452.b09-1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=1.8.0_452.b09-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:68b5eef1eb563a36e20df422ee1592c70689019fdd12cc4fdc4e4b24c31c1c77`  
		Last Modified: Thu, 27 Mar 2025 19:19:22 GMT  
		Size: 62.8 MB (62752889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b44df2aa9be9a7dcf5d4ca6579bc5fe493b1adf3c4c8d0e66a6c852521a5d85`  
		Last Modified: Tue, 15 Apr 2025 23:55:57 GMT  
		Size: 109.1 MB (109091706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u452-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:01a7df7d8e9709edc734c0c69ee4dbba4ec22f384e23c61c44aaf66a4a1b6787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7493002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfb14368ded1ccdf018075f9717b41ef191b0db07e973ac4bed7b89586f71b35`

```dockerfile
```

-	Layers:
	-	`sha256:8e374313ef9623ec426a6ff11e74101df96615c6bcc4566d8829653e2a258543`  
		Last Modified: Tue, 15 Apr 2025 23:55:54 GMT  
		Size: 7.5 MB (7483455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:622098069a4649c0b40b92aad69a5164af8fa8b35350733726b71ba167cfc748`  
		Last Modified: Tue, 15 Apr 2025 23:55:54 GMT  
		Size: 9.5 KB (9547 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u452-al2-native-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b3b53bfde27ce543f01e01656b1fd7e6af3dc3b82907f69252e6b628454e837e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **117.5 MB (117482296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac3121d17d213087b81f46b7b15100ea441f669cfdefa288112ca2327ac0d7db`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Mar 2025 17:58:42 GMT
COPY /rootfs/ / # buildkit
# Thu, 27 Mar 2025 17:58:42 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=1.8.0_452.b09-1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=1.8.0_452.b09-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && echo $(rpm -K "${CORRETO_TEMP}/${rpm}")     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1;     done     && yum install -y $(yum deplist ${CORRETO_TEMP}/*.rpm |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 )     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto/jre
```

-	Layers:
	-	`sha256:bf0d47d55e313b24603bbdfcf71df5fce9b23e8a6af770024f7d7c0282dd1e60`  
		Last Modified: Thu, 27 Mar 2025 19:19:37 GMT  
		Size: 64.6 MB (64565822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15cc0a2b7037bee9bdfb899f430aa98a69db495eaaf744d349d1fbad3e78fa04`  
		Last Modified: Tue, 15 Apr 2025 23:56:46 GMT  
		Size: 52.9 MB (52916474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u452-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:262b4dea11c38baefa94a2668a64b9c5aac5e6b3fa1f9239d665177eedbdc4e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5612458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:037e2b0ef2cf0f0298dc58f201a7d06e1cbd40a0c4790c73d7398e4c3ca44722`

```dockerfile
```

-	Layers:
	-	`sha256:3a181dd3326f71953d5c36777a6431e7289e86d3715861efdb80e8fd85c11c89`  
		Last Modified: Tue, 15 Apr 2025 23:56:45 GMT  
		Size: 5.6 MB (5602832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a363cf1406467f528f6fb6d7c23ee5b3b8ee3b893f0e639fe6dcce1cbd3e7920`  
		Last Modified: Tue, 15 Apr 2025 23:56:44 GMT  
		Size: 9.6 KB (9626 bytes)  
		MIME: application/vnd.in-toto+json
