## `amazoncorretto:8-al2-native-jre`

```console
$ docker pull amazoncorretto@sha256:a940ca9f8d0ade063951304fa089e1290acd675659b3cfe755bd8b7c8871d2b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-al2-native-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:453b88a26597eda6b44cc448f9881c41f026ebde1eea2e99be8312b36ebd7e20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.9 MB (171877893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13151d8bfdaa10eeba83d018ce67cfce2b35f89063070d08a03e5ae6e38652bc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Apr 2025 21:50:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
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
	-	`sha256:07f9ec6a4553009171ec20ecdc638afd0eaac432b31f9e1b569f6e4fe9454d93`  
		Last Modified: Mon, 21 Apr 2025 21:48:34 GMT  
		Size: 62.8 MB (62761722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8431a700718d39b9a71d46bc346a608e1d04fabed545f3f72950eb19345c4cb6`  
		Last Modified: Thu, 24 Apr 2025 20:08:15 GMT  
		Size: 109.1 MB (109116171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3026531a54b6fc5bf3ab0fa4f547e2664258fef0b972403ff262b4701de458ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7494889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cbbd8fa300e920d341c6c253b90756d1cd92bee8698a4fd9916c5c20aca37f7`

```dockerfile
```

-	Layers:
	-	`sha256:2d7a48122f71b9336850e0ebde4b1b9e812519d44e7e3bba3b11edd948acbf28`  
		Last Modified: Thu, 24 Apr 2025 20:08:13 GMT  
		Size: 7.5 MB (7485341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a602bd37b018f2e6e7b1df88c9bce8c84d71f6bb6f7f3f5cb817862823f5d453`  
		Last Modified: Thu, 24 Apr 2025 20:08:13 GMT  
		Size: 9.5 KB (9548 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-al2-native-jre` - linux; arm64 variant v8

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

### `amazoncorretto:8-al2-native-jre` - unknown; unknown

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
